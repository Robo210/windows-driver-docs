---
title: NET_BUFFER_LIST Structure Macros
author: windows-driver-content
description: NET_BUFFER_LIST Structure Macros
ms.assetid: b3979a02-2367-468f-af25-9ece28e14ccb
ms.author: windowsdriverdev 
ms.date: 07/18/2017 
ms.topic: article 
ms.prod: windows-hardware 
ms.technology: windows-devices
---

# NET\_BUFFER\_LIST Structure Macros


## <a href="" id="ddk-net-buffer-list-structure-macros-nr"></a>


This section includes:

## In this section


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Topic</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>[<strong>NDIS_NBL_ADD_MEDIA_SPECIFIC_INFO</strong>](ndis-nbl-add-media-specific-info.md)</p></td>
<td><p>The [<strong>NDIS_NBL_ADD_MEDIA_SPECIFIC_INFO</strong>](ndis-nbl-add-media-specific-info.md) macro adds a media-specific information data structure to the beginning of a linked list of such structures that are associated with a [<strong>NET_BUFFER_LIST</strong>](https://msdn.microsoft.com/library/windows/hardware/ff568388) structure.</p></td>
</tr>
<tr class="even">
<td><p>[<strong>NDIS_NBL_ADD_MEDIA_SPECIFIC_INFO_EX</strong>](ndis-nbl-add-media-specific-info-ex.md)</p></td>
<td><p>The NDIS_NBL_ADD_MEDIA_SPECIFIC_INFO_EX macro adds a media-specific information data structure to the beginning of a linked list of such structures that are associated with a [<strong>NET_BUFFER_LIST</strong>](https://msdn.microsoft.com/library/windows/hardware/ff568388) structure.</p></td>
</tr>
<tr class="odd">
<td><p>[<strong>NDIS_NBL_GET_MEDIA_SPECIFIC_INFO</strong>](ndis-nbl-get-media-specific-info.md)</p></td>
<td><p>The NDIS_NBL_GET_MEDIA_SPECIFIC_INFO macro gets a media-specific information data structure from a linked list of such structures that are associated with a [<strong>NET_BUFFER_LIST</strong>](https://msdn.microsoft.com/library/windows/hardware/ff568388) structure.</p></td>
</tr>
<tr class="even">
<td><p>[<strong>NDIS_NBL_GET_MEDIA_SPECIFIC_INFO_EX</strong>](ndis-nbl-get-media-specific-info-ex.md)</p></td>
<td><p>The [<strong>NDIS_NBL_GET_MEDIA_SPECIFIC_INFO_EX</strong>](ndis-nbl-get-media-specific-info-ex.md) macro gets a media-specific information data structure from a linked list of such structures that are associated with a [<strong>NET_BUFFER_LIST</strong>](https://msdn.microsoft.com/library/windows/hardware/ff568388) structure.</p></td>
</tr>
<tr class="odd">
<td><p>[<strong>NDIS_NBL_REMOVE_MEDIA_SPECIFIC_INFO</strong>](ndis-nbl-remove-media-specific-info.md)</p></td>
<td><p>The NDIS_NBL_REMOVE_MEDIA_SPECIFIC_INFO macro removes a media-specific information data structure from a linked list of such structures that are associated with a [<strong>NET_BUFFER_LIST</strong>](https://msdn.microsoft.com/library/windows/hardware/ff568388) structure.</p></td>
</tr>
<tr class="even">
<td><p>[<strong>NDIS_NBL_REMOVE_MEDIA_SPECIFIC_INFO_EX</strong>](ndis-nbl-remove-media-specific-info-ex.md)</p></td>
<td><p>The [<strong>NDIS_NBL_REMOVE_MEDIA_SPECIFIC_INFO_EX</strong>](ndis-nbl-remove-media-specific-info-ex.md) macro removes a media-specific information data structure from a linked list of such structures that are associated with a [<strong>NET_BUFFER_LIST</strong>](https://msdn.microsoft.com/library/windows/hardware/ff568388) structure.</p></td>
</tr>
<tr class="odd">
<td><p>[<strong>NdisSetNetBufferListProtocolId</strong>](ndissetnetbufferlistprotocolid.md)</p></td>
<td><p>The <strong>NdisSetNetBufferListProtocolId</strong> macro sets the protocol identifier in the <strong>NetBufferListInfo</strong> member of a [<strong>NET_BUFFER_LIST</strong>](https://msdn.microsoft.com/library/windows/hardware/ff568388) structure.</p></td>
</tr>
<tr class="even">
<td><p>[<strong>NET_BUFFER_LIST_CONTEXT_DATA_SIZE</strong>](net-buffer-list-context-data-size.md)</p></td>
<td><p>NET_BUFFER_LIST_CONTEXT_DATA_SIZE is a macro that NDIS drivers use to get the size of the [<strong>NET_BUFFER_LIST_CONTEXT</strong>](https://msdn.microsoft.com/library/windows/hardware/ff568389) data buffer that is associated with a [<strong>NET_BUFFER_LIST</strong>](https://msdn.microsoft.com/library/windows/hardware/ff568388) structure.</p></td>
</tr>
<tr class="odd">
<td><p>[<strong>NET_BUFFER_LIST_CONTEXT_DATA_START</strong>](net-buffer-list-context-data-start.md)</p></td>
<td><p>NET_BUFFER_LIST_CONTEXT_DATA_START is a macro that NDIS drivers use to get a pointer to the [<strong>NET_BUFFER_LIST_CONTEXT</strong>](https://msdn.microsoft.com/library/windows/hardware/ff568389) context space that is associated with a [<strong>NET_BUFFER_LIST</strong>](https://msdn.microsoft.com/library/windows/hardware/ff568388) structure.</p></td>
</tr>
<tr class="even">
<td><p>[<strong>NET_BUFFER_LIST_FIRST_NB</strong>](net-buffer-list-first-nb.md)</p></td>
<td><p>NET_BUFFER_LIST_FIRST_NB is a macro that NDIS drivers use to get the first [<strong>NET_BUFFER</strong>](https://msdn.microsoft.com/library/windows/hardware/ff568376) structure in a [<strong>NET_BUFFER_LIST</strong>](https://msdn.microsoft.com/library/windows/hardware/ff568388) structure.</p></td>
</tr>
<tr class="odd">
<td><p>[<strong>NET_BUFFER_LIST_FLAGS</strong>](net-buffer-list-flags.md)</p></td>
<td><p>NET_BUFFER_LIST_FLAGS is a macro that NDIS drivers use to get the flags associated with a [<strong>NET_BUFFER_LIST</strong>](https://msdn.microsoft.com/library/windows/hardware/ff568388) structure.</p></td>
</tr>
<tr class="even">
<td><p>[<strong>NET_BUFFER_LIST_MINIPORT_RESERVED</strong>](net-buffer-list-miniport-reserved.md)</p></td>
<td><p>NET_BUFFER_LIST_MINIPORT_RESERVED is a macro that NDIS drivers use to access the <strong>MiniportReserved</strong> member of a [<strong>NET_BUFFER_LIST</strong>](https://msdn.microsoft.com/library/windows/hardware/ff568388) structure.</p></td>
</tr>
<tr class="odd">
<td><p>[<strong>NET_BUFFER_LIST_NEXT_NBL</strong>](net-buffer-list-next-nbl.md)</p></td>
<td><p>NET_BUFFER_LIST_NEXT_NBL is a macro that NDIS drivers use to get the next [<strong>NET_BUFFER_LIST</strong>](https://msdn.microsoft.com/library/windows/hardware/ff568388) structure in a linked list of NET_BUFFER_LIST structures.</p></td>
</tr>
<tr class="even">
<td><p>[<strong>NET_BUFFER_LIST_INFO</strong>](net-buffer-list-info.md)</p></td>
<td><p>NET_BUFFER_LIST_INFO is a macro that NDIS drivers use to get and set information that applies to all the [<strong>NET_BUFFER</strong>](https://msdn.microsoft.com/library/windows/hardware/ff568376) structures in a [<strong>NET_BUFFER_LIST</strong>](https://msdn.microsoft.com/library/windows/hardware/ff568388) structure.</p></td>
</tr>
<tr class="odd">
<td><p>[<strong>NET_BUFFER_LIST_STATUS</strong>](net-buffer-list-status.md)</p></td>
<td><p>NET_BUFFER_LIST_STATUS is a macro that NDIS drivers use to access the <strong>StatusCode</strong> member of a [<strong>NET_BUFFER_LIST</strong>](https://msdn.microsoft.com/library/windows/hardware/ff568388) structure.</p></td>
</tr>
<tr class="even">
<td><p>[<strong>NET_BUFFER_LIST_PROTOCOL_RESERVED</strong>](net-buffer-list-protocol-reserved.md)</p></td>
<td><p>NET_BUFFER_LIST_PROTOCOL_RESERVED is a macro that NDIS drivers use to access the <strong>ProtocolReserved</strong> member of a [<strong>NET_BUFFER_LIST</strong>](https://msdn.microsoft.com/library/windows/hardware/ff568388) structure.</p></td>
</tr>
<tr class="odd">
<td><p>[<strong>NET_BUFFER_LIST_RECEIVE_FILTER_ID</strong>](net-buffer-list-receive-filter-id.md)</p></td>
<td><p>The NET_BUFFER_LIST_RECEIVE_FILTER_ID macro gets a receive filter identifier from the out-of-band (OOB) data in a [<strong>NET_BUFFER_LIST</strong>](https://msdn.microsoft.com/library/windows/hardware/ff568388) structure.</p></td>
</tr>
</tbody>
</table>

 

 

 




