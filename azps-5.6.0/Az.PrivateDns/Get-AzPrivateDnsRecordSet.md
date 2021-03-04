---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/powershell/module/az.privatedns/get-azprivatednsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Get-AzPrivateDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Get-AzPrivateDnsRecordSet.md
ms.openlocfilehash: 7ddc6b9621bbf156b386a0f67337edcc32e0363c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917665"
---
# <span data-ttu-id="09927-101">Get-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="09927-101">Get-AzPrivateDnsRecordSet</span></span>

## <span data-ttu-id="09927-102">簡介</span><span class="sxs-lookup"><span data-stu-id="09927-102">SYNOPSIS</span></span>
<span data-ttu-id="09927-103">從私人 DNS 區域獲得記錄集。</span><span class="sxs-lookup"><span data-stu-id="09927-103">Gets a record set from a Private DNS zone.</span></span>

## <span data-ttu-id="09927-104">語法</span><span class="sxs-lookup"><span data-stu-id="09927-104">SYNTAX</span></span>

### <span data-ttu-id="09927-105">FieldsWithNoName (預設) </span><span class="sxs-lookup"><span data-stu-id="09927-105">FieldsWithNoName (Default)</span></span>
```
Get-AzPrivateDnsRecordSet -ResourceGroupName <String> -ZoneName <String> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="09927-106">領域</span><span class="sxs-lookup"><span data-stu-id="09927-106">Fields</span></span>
```
Get-AzPrivateDnsRecordSet -ResourceGroupName <String> -ZoneName <String> -Name <String>
 -RecordType <RecordType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="09927-107">物件</span><span class="sxs-lookup"><span data-stu-id="09927-107">Object</span></span>
```
Get-AzPrivateDnsRecordSet -Zone <PSPrivateDnsZone> -Name <String> -RecordType <RecordType>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="09927-108">ObjectWithNoName</span><span class="sxs-lookup"><span data-stu-id="09927-108">ObjectWithNoName</span></span>
```
Get-AzPrivateDnsRecordSet -Zone <PSPrivateDnsZone> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="09927-109">ResourceId</span><span class="sxs-lookup"><span data-stu-id="09927-109">ResourceId</span></span>
```
Get-AzPrivateDnsRecordSet -ParentResourceId <String> -Name <String> -RecordType <RecordType>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="09927-110">ResourceIdWithNoName</span><span class="sxs-lookup"><span data-stu-id="09927-110">ResourceIdWithNoName</span></span>
```
Get-AzPrivateDnsRecordSet -ParentResourceId <String> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="09927-111">描述</span><span class="sxs-lookup"><span data-stu-id="09927-111">DESCRIPTION</span></span>
<span data-ttu-id="09927-112">此Get-AzPrivateDnsRecordSet Cmdlet 會 (專用網域名稱系統) 指定名稱和類型的 DNS 記錄集，並設定于指定的私人區域中。</span><span class="sxs-lookup"><span data-stu-id="09927-112">The Get-AzPrivateDnsRecordSet cmdlet gets the Private Domain Name System (DNS) record set with the specified name and type, in the specified private zone.</span></span> <span data-ttu-id="09927-113">如果您未指定 Name 或 RecordType 參數，此 Cmdlet 會傳回私人區域中指定類型的所有記錄集。</span><span class="sxs-lookup"><span data-stu-id="09927-113">If you do not specify the Name or RecordType parameters, this cmdlet returns all record sets of the specified type in the private zone.</span></span> <span data-ttu-id="09927-114">如果您指定 RecordType 參數，但未指定 Name 參數，此 Cmdlet 會傳回指定記錄類型的所有記錄集。</span><span class="sxs-lookup"><span data-stu-id="09927-114">If you specify the RecordType parameter but not the Name parameter, this cmdlet returns all record sets of the specified record type.</span></span> <span data-ttu-id="09927-115">您可以使用管線運算子將 PSPrivateDnsZone 物件傳遞至此 Cmdlet，或將 PSPrivateDnsZone 物件傳遞為 Zone 參數，或者您也可以按名稱指定區域和資源群組。</span><span class="sxs-lookup"><span data-stu-id="09927-115">You can use the pipeline operator to pass a PSPrivateDnsZone object to this cmdlet, or you can pass a PSPrivateDnsZone object as the Zone parameter, or alternatively you can specify the zone and resource group by name.</span></span> <span data-ttu-id="09927-116">您也可以使用私人區域的資源識別碼指定私人區域。</span><span class="sxs-lookup"><span data-stu-id="09927-116">You can also specify the private zone using the Resource Id of the private zone.</span></span>

## <span data-ttu-id="09927-117">例子</span><span class="sxs-lookup"><span data-stu-id="09927-117">EXAMPLES</span></span>

### <span data-ttu-id="09927-118">範例 1：取得具有指定名稱和類型的記錄集</span><span class="sxs-lookup"><span data-stu-id="09927-118">Example 1: Get record sets with a specified name and type</span></span>
```powershell
PS C:\>$RecordSet = Get-AzPrivateDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -Name "www" -RecordType A

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {1.2.3.4}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="09927-119">此命令會獲得指定資源群組和私人區域中名為 www 的記錄類型 A 記錄集，然後將它儲存在$RecordSet變數。</span><span class="sxs-lookup"><span data-stu-id="09927-119">This command gets the record set of record type A named www in the specified resource group and private zone, and then stores it in the $RecordSet variable.</span></span> <span data-ttu-id="09927-120">由於會指定 Name 和 RecordType 參數，因此只會傳回一個 RecordSet 物件。</span><span class="sxs-lookup"><span data-stu-id="09927-120">Because the Name and RecordType parameters are specified, only one RecordSet object is returned.</span></span>

### <span data-ttu-id="09927-121">範例 2：取得指定類型的記錄集</span><span class="sxs-lookup"><span data-stu-id="09927-121">Example 2: Get record sets of a specified type</span></span>
```powershell
PS C:\>$RecordSets = Get-AzPrivateDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -RecordType A

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www1
Name              : www1
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {1.2.3.4}
Metadata          :
IsAutoRegistered  :

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www2
Name              : www2
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {2.3.4.5}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="09927-122">此命令會從名為 MyResourceGroup 的資源群組中，將 A 記錄類型的所有記錄集陣列放在名為 myzone.com 的私人區域中，然後將它們儲存在 $RecordSets 變數中。</span><span class="sxs-lookup"><span data-stu-id="09927-122">This command gets an array of all record sets of record type A in the private zone named myzone.com in the resource group named MyResourceGroup, and then stores them in the $RecordSets variable.</span></span>

### <span data-ttu-id="09927-123">範例 3：取得私人區域中的所有記錄集</span><span class="sxs-lookup"><span data-stu-id="09927-123">Example 3: Get all record sets in a private zone</span></span>
```powershell
PS C:\>$RecordSets = Get-AzPrivateDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www1
Name              : www1
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {1.2.3.4}
Metadata          :
IsAutoRegistered  :

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www1
Name              : www1
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : AAAA
Records           : {2001:DB80:4009:1803::1005}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="09927-124">此命令會從名為 MyResourceGroup 的資源群組中，于私人區域中myzone.com記錄集的陣列，然後將這些記錄集儲存在 $RecordSets 變數中。</span><span class="sxs-lookup"><span data-stu-id="09927-124">This command gets an array of all record sets in the private zone named myzone.com in the resource group named MyResourceGroup, and then stores them in the $RecordSets variable.</span></span>

### <span data-ttu-id="09927-125">範例 4：使用 PSPrivateDnsZone 物件取得私人區域中的所有記錄集</span><span class="sxs-lookup"><span data-stu-id="09927-125">Example 4: Get all record sets in a private zone, using a PSPrivateDnsZone object</span></span>
```powershell
PS C:\> $Zone = Get-AzPrivateDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $RecordSets = Get-AzPrivateDnsRecordSet -Zone $Zone

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www1
Name              : www1
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {1.2.3.4}
Metadata          :
IsAutoRegistered  :

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www1
Name              : www1
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : AAAA
Records           : {2001:DB80:4009:1803::1005}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="09927-126">此範例相當於上述範例 3。</span><span class="sxs-lookup"><span data-stu-id="09927-126">This example is equivalent to Example 3 above.</span></span> <span data-ttu-id="09927-127">這次，私人區域是使用私人區域物件指定。</span><span class="sxs-lookup"><span data-stu-id="09927-127">This time, the private zone is specified using a private zone object.</span></span>

## <span data-ttu-id="09927-128">參數</span><span class="sxs-lookup"><span data-stu-id="09927-128">PARAMETERS</span></span>

### <span data-ttu-id="09927-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09927-129">-DefaultProfile</span></span>
<span data-ttu-id="09927-130">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="09927-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09927-131">-名稱</span><span class="sxs-lookup"><span data-stu-id="09927-131">-Name</span></span>
<span data-ttu-id="09927-132">此記錄集的記錄名稱會 (區功能變數名稱稱相關，且不含終止點) 。</span><span class="sxs-lookup"><span data-stu-id="09927-132">The name of the records in this record set (relative to the name of the zone and without a terminating dot).</span></span>

```yaml
Type: System.String
Parameter Sets: Fields, Object, ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09927-133">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="09927-133">-ParentResourceId</span></span>
<span data-ttu-id="09927-134">私人 DNS 區域資源ID。</span><span class="sxs-lookup"><span data-stu-id="09927-134">Private DNS Zone ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId, ResourceIdWithNoName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09927-135">-RecordType</span><span class="sxs-lookup"><span data-stu-id="09927-135">-RecordType</span></span>
<span data-ttu-id="09927-136">此記錄集的 DNS 記錄類型。</span><span class="sxs-lookup"><span data-stu-id="09927-136">The type of DNS records in this record set.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.PrivateDns.Models.RecordType]
Parameter Sets: FieldsWithNoName, ObjectWithNoName, ResourceIdWithNoName
Aliases:
Accepted values: A, AAAA, CNAME, MX, PTR, SOA, SRV, TXT

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.PrivateDns.Models.RecordType]
Parameter Sets: Fields, Object, ResourceId
Aliases:
Accepted values: A, AAAA, CNAME, MX, PTR, SOA, SRV, TXT

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09927-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09927-137">-ResourceGroupName</span></span>
<span data-ttu-id="09927-138">區域所屬的資源群組。</span><span class="sxs-lookup"><span data-stu-id="09927-138">The resource group to which the zone belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: FieldsWithNoName, Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09927-139">-區域</span><span class="sxs-lookup"><span data-stu-id="09927-139">-Zone</span></span>
<span data-ttu-id="09927-140">代表要建立記錄集之區域之 DnsZone 物件。</span><span class="sxs-lookup"><span data-stu-id="09927-140">The DnsZone object representing the zone in which to create the record set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone
Parameter Sets: Object, ObjectWithNoName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="09927-141">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="09927-141">-ZoneName</span></span>
<span data-ttu-id="09927-142">建立記錄集的區域 (終止點) 。</span><span class="sxs-lookup"><span data-stu-id="09927-142">The zone in which to create the record set (without a terminating dot).</span></span>

```yaml
Type: System.String
Parameter Sets: FieldsWithNoName, Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09927-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09927-143">CommonParameters</span></span>
<span data-ttu-id="09927-144">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="09927-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09927-145">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="09927-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09927-146">輸入</span><span class="sxs-lookup"><span data-stu-id="09927-146">INPUTS</span></span>

### <span data-ttu-id="09927-147">Microsoft.Azure.Commands.PrivateDns.models.PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="09927-147">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

### <span data-ttu-id="09927-148">System.String</span><span class="sxs-lookup"><span data-stu-id="09927-148">System.String</span></span>

## <span data-ttu-id="09927-149">輸出</span><span class="sxs-lookup"><span data-stu-id="09927-149">OUTPUTS</span></span>

### <span data-ttu-id="09927-150">Microsoft.Azure.Commands.PrivateDns.models.PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="09927-150">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="09927-151">筆記</span><span class="sxs-lookup"><span data-stu-id="09927-151">NOTES</span></span>

## <span data-ttu-id="09927-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="09927-152">RELATED LINKS</span></span>
