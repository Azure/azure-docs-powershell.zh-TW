---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/get-azprivatednsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Get-AzPrivateDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Get-AzPrivateDnsRecordSet.md
ms.openlocfilehash: a0b527a0931c5c3423e5e64bad0abb7128fc3497
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621233"
---
# <span data-ttu-id="b3fac-101">Get-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="b3fac-101">Get-AzPrivateDnsRecordSet</span></span>

## <span data-ttu-id="b3fac-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b3fac-102">SYNOPSIS</span></span>
<span data-ttu-id="b3fac-103">從私有 DNS 區域取得記錄集。</span><span class="sxs-lookup"><span data-stu-id="b3fac-103">Gets a record set from a Private DNS zone.</span></span>

## <span data-ttu-id="b3fac-104">句法</span><span class="sxs-lookup"><span data-stu-id="b3fac-104">SYNTAX</span></span>

### <span data-ttu-id="b3fac-105">FieldsWithNoName (預設) </span><span class="sxs-lookup"><span data-stu-id="b3fac-105">FieldsWithNoName (Default)</span></span>
```
Get-AzPrivateDnsRecordSet -ResourceGroupName <String> -ZoneName <String> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3fac-106">區域</span><span class="sxs-lookup"><span data-stu-id="b3fac-106">Fields</span></span>
```
Get-AzPrivateDnsRecordSet -ResourceGroupName <String> -ZoneName <String> -Name <String>
 -RecordType <RecordType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3fac-107">面向</span><span class="sxs-lookup"><span data-stu-id="b3fac-107">Object</span></span>
```
Get-AzPrivateDnsRecordSet -Zone <PSPrivateDnsZone> -Name <String> -RecordType <RecordType>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3fac-108">ObjectWithNoName</span><span class="sxs-lookup"><span data-stu-id="b3fac-108">ObjectWithNoName</span></span>
```
Get-AzPrivateDnsRecordSet -Zone <PSPrivateDnsZone> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3fac-109">ResourceId</span><span class="sxs-lookup"><span data-stu-id="b3fac-109">ResourceId</span></span>
```
Get-AzPrivateDnsRecordSet -ParentResourceId <String> -Name <String> -RecordType <RecordType>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3fac-110">ResourceIdWithNoName</span><span class="sxs-lookup"><span data-stu-id="b3fac-110">ResourceIdWithNoName</span></span>
```
Get-AzPrivateDnsRecordSet -ParentResourceId <String> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b3fac-111">說明</span><span class="sxs-lookup"><span data-stu-id="b3fac-111">DESCRIPTION</span></span>
<span data-ttu-id="b3fac-112">Get-AzPrivateDnsRecordSet Cmdlet 會在指定的私人區域中，以指定的名稱與類型 (DNS) 記錄，取得私人網功能變數名稱稱系統。</span><span class="sxs-lookup"><span data-stu-id="b3fac-112">The Get-AzPrivateDnsRecordSet cmdlet gets the Private Domain Name System (DNS) record set with the specified name and type, in the specified private zone.</span></span> <span data-ttu-id="b3fac-113">如果您沒有指定 Name 或 RecordType 參數，這個 Cmdlet 會傳回私人區域中指定類型的所有記錄集。</span><span class="sxs-lookup"><span data-stu-id="b3fac-113">If you do not specify the Name or RecordType parameters, this cmdlet returns all record sets of the specified type in the private zone.</span></span> <span data-ttu-id="b3fac-114">如果您指定 RecordType 參數而不是 Name 參數，這個 Cmdlet 會傳回指定記錄類型的所有記錄集。</span><span class="sxs-lookup"><span data-stu-id="b3fac-114">If you specify the RecordType parameter but not the Name parameter, this cmdlet returns all record sets of the specified record type.</span></span> <span data-ttu-id="b3fac-115">您可以使用管線運算子，將 PSPrivateDnsZone 物件傳遞到這個 Cmdlet，或者您可以將 PSPrivateDnsZone 物件傳遞為 Zone 參數，或者也可以依名稱指定區域和資源群組。</span><span class="sxs-lookup"><span data-stu-id="b3fac-115">You can use the pipeline operator to pass a PSPrivateDnsZone object to this cmdlet, or you can pass a PSPrivateDnsZone object as the Zone parameter, or alternatively you can specify the zone and resource group by name.</span></span> <span data-ttu-id="b3fac-116">您也可以使用私人區域的資源識別碼來指定私人區域。</span><span class="sxs-lookup"><span data-stu-id="b3fac-116">You can also specify the private zone using the Resource Id of the private zone.</span></span>

## <span data-ttu-id="b3fac-117">示例</span><span class="sxs-lookup"><span data-stu-id="b3fac-117">EXAMPLES</span></span>

### <span data-ttu-id="b3fac-118">範例1：取得具有指定名稱和類型的記錄集</span><span class="sxs-lookup"><span data-stu-id="b3fac-118">Example 1: Get record sets with a specified name and type</span></span>
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

<span data-ttu-id="b3fac-119">這個命令會在指定的 [資源] 群組和 [私人區域] 中取得一組記錄類型的記錄，並將它儲存在 $RecordSet 變數中。</span><span class="sxs-lookup"><span data-stu-id="b3fac-119">This command gets the record set of record type A named www in the specified resource group and private zone, and then stores it in the $RecordSet variable.</span></span> <span data-ttu-id="b3fac-120">因為已指定 Name 和 RecordType 參數，所以只會傳回一個記錄集物件。</span><span class="sxs-lookup"><span data-stu-id="b3fac-120">Because the Name and RecordType parameters are specified, only one RecordSet object is returned.</span></span>

### <span data-ttu-id="b3fac-121">範例2：取得指定類型的記錄集</span><span class="sxs-lookup"><span data-stu-id="b3fac-121">Example 2: Get record sets of a specified type</span></span>
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

<span data-ttu-id="b3fac-122">這個命令會在名為 MyResourceGroup 的資源群組中，從名為 myzone.com 的私人區域中，取得記錄類型 A 的所有記錄集的陣列，然後將它們儲存在 $RecordSets 變數中。</span><span class="sxs-lookup"><span data-stu-id="b3fac-122">This command gets an array of all record sets of record type A in the private zone named myzone.com in the resource group named MyResourceGroup, and then stores them in the $RecordSets variable.</span></span>

### <span data-ttu-id="b3fac-123">範例3：取得私人區域中的所有記錄集</span><span class="sxs-lookup"><span data-stu-id="b3fac-123">Example 3: Get all record sets in a private zone</span></span>
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

<span data-ttu-id="b3fac-124">這個命令會在名為 [MyResourceGroup] 的資源群組中，取得名為 myzone.com 的私人區域中所有記錄集的陣列，然後將它們儲存在 $RecordSets 變數中。</span><span class="sxs-lookup"><span data-stu-id="b3fac-124">This command gets an array of all record sets in the private zone named myzone.com in the resource group named MyResourceGroup, and then stores them in the $RecordSets variable.</span></span>

### <span data-ttu-id="b3fac-125">範例4：使用 PSPrivateDnsZone 物件在私有區域中取得所有記錄集</span><span class="sxs-lookup"><span data-stu-id="b3fac-125">Example 4: Get all record sets in a private zone, using a PSPrivateDnsZone object</span></span>
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

<span data-ttu-id="b3fac-126">這個範例與上述範例3相當。</span><span class="sxs-lookup"><span data-stu-id="b3fac-126">This example is equivalent to Example 3 above.</span></span> <span data-ttu-id="b3fac-127">這次會使用私人區域物件來指定私人區域。</span><span class="sxs-lookup"><span data-stu-id="b3fac-127">This time, the private zone is specified using a private zone object.</span></span>

## <span data-ttu-id="b3fac-128">參數</span><span class="sxs-lookup"><span data-stu-id="b3fac-128">PARAMETERS</span></span>

### <span data-ttu-id="b3fac-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3fac-129">-DefaultProfile</span></span>
<span data-ttu-id="b3fac-130">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b3fac-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3fac-131">-名稱</span><span class="sxs-lookup"><span data-stu-id="b3fac-131">-Name</span></span>
<span data-ttu-id="b3fac-132">此記錄集中的記錄名稱 (相對於區域的名稱，且不需要終止點) 。</span><span class="sxs-lookup"><span data-stu-id="b3fac-132">The name of the records in this record set (relative to the name of the zone and without a terminating dot).</span></span>

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

### <span data-ttu-id="b3fac-133">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="b3fac-133">-ParentResourceId</span></span>
<span data-ttu-id="b3fac-134">私人 DNS 區域 ResourceID。</span><span class="sxs-lookup"><span data-stu-id="b3fac-134">Private DNS Zone ResourceID.</span></span>

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

### <span data-ttu-id="b3fac-135">-RecordType</span><span class="sxs-lookup"><span data-stu-id="b3fac-135">-RecordType</span></span>
<span data-ttu-id="b3fac-136">此記錄集中的 DNS 記錄類型。</span><span class="sxs-lookup"><span data-stu-id="b3fac-136">The type of DNS records in this record set.</span></span>

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

### <span data-ttu-id="b3fac-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3fac-137">-ResourceGroupName</span></span>
<span data-ttu-id="b3fac-138">該區域所屬的資源群組。</span><span class="sxs-lookup"><span data-stu-id="b3fac-138">The resource group to which the zone belongs.</span></span>

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

### <span data-ttu-id="b3fac-139">-Zone</span><span class="sxs-lookup"><span data-stu-id="b3fac-139">-Zone</span></span>
<span data-ttu-id="b3fac-140">代表要在其中建立記錄集之區域的 DnsZone 物件。</span><span class="sxs-lookup"><span data-stu-id="b3fac-140">The DnsZone object representing the zone in which to create the record set.</span></span>

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

### <span data-ttu-id="b3fac-141">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="b3fac-141">-ZoneName</span></span>
<span data-ttu-id="b3fac-142">在其中建立記錄集的區域 (，不需終止點) 。</span><span class="sxs-lookup"><span data-stu-id="b3fac-142">The zone in which to create the record set (without a terminating dot).</span></span>

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

### <span data-ttu-id="b3fac-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3fac-143">CommonParameters</span></span>
<span data-ttu-id="b3fac-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b3fac-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3fac-145">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b3fac-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3fac-146">輸入</span><span class="sxs-lookup"><span data-stu-id="b3fac-146">INPUTS</span></span>

### <span data-ttu-id="b3fac-147">PSPrivateDnsZone 中的 PrivateDns。</span><span class="sxs-lookup"><span data-stu-id="b3fac-147">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

### <span data-ttu-id="b3fac-148">System.object</span><span class="sxs-lookup"><span data-stu-id="b3fac-148">System.String</span></span>

## <span data-ttu-id="b3fac-149">輸出</span><span class="sxs-lookup"><span data-stu-id="b3fac-149">OUTPUTS</span></span>

### <span data-ttu-id="b3fac-150">PSPrivateDnsRecordSet 中的 PrivateDns。</span><span class="sxs-lookup"><span data-stu-id="b3fac-150">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="b3fac-151">筆記</span><span class="sxs-lookup"><span data-stu-id="b3fac-151">NOTES</span></span>

## <span data-ttu-id="b3fac-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="b3fac-152">RELATED LINKS</span></span>
