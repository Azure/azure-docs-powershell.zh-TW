---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/powershell/module/az.privatedns/Set-AzPrivateDnsRecordSet
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsRecordSet.md
ms.openlocfilehash: 68e55ae6a0c563ecc72e74fc127360ddb35f73f3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910677"
---
# <span data-ttu-id="d1953-101">Set-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="d1953-101">Set-AzPrivateDnsRecordSet</span></span>

## <span data-ttu-id="d1953-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d1953-102">SYNOPSIS</span></span>
<span data-ttu-id="d1953-103">更新/設定私人 DNS 區域中的記錄集。</span><span class="sxs-lookup"><span data-stu-id="d1953-103">Updates/Sets a record set in a Private DNS zone.</span></span>

## <span data-ttu-id="d1953-104">語法</span><span class="sxs-lookup"><span data-stu-id="d1953-104">SYNTAX</span></span>

```
Set-AzPrivateDnsRecordSet -RecordSet <PSPrivateDnsRecordSet> [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d1953-105">描述</span><span class="sxs-lookup"><span data-stu-id="d1953-105">DESCRIPTION</span></span>
<span data-ttu-id="d1953-106">Cmdlet Set-AzPrivateDnsRecordSet從本地 RecordSet 物件更新 Azure Private DNS 服務中的記錄集。</span><span class="sxs-lookup"><span data-stu-id="d1953-106">The Set-AzPrivateDnsRecordSet cmdlet updates a record set in the Azure Private DNS service from a local RecordSet object.</span></span> <span data-ttu-id="d1953-107">您可以將 RecordSet 物件傳遞為參數，或是使用管線運算子。</span><span class="sxs-lookup"><span data-stu-id="d1953-107">You can pass a RecordSet object as a parameter or by using the pipeline operator.</span></span> <span data-ttu-id="d1953-108">您可以使用確認參數$ConfirmPreference Windows PowerShell 變數來控制 Cmdlet 是否提示您確認。</span><span class="sxs-lookup"><span data-stu-id="d1953-108">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span> <span data-ttu-id="d1953-109">如果記錄集在 Azure Private DNS 中自本地 RecordSet 物件被取回之後已經變更，則記錄集不會更新。</span><span class="sxs-lookup"><span data-stu-id="d1953-109">The record set is not updated if it has been changed in Azure Private DNS since the local RecordSet object was retrieved.</span></span> <span data-ttu-id="d1953-110">這可保護同時進行變更。</span><span class="sxs-lookup"><span data-stu-id="d1953-110">This provides protection for concurrent changes.</span></span> <span data-ttu-id="d1953-111">您可以使用覆寫參數隱藏此行為，無論同時變更，都會更新記錄集。</span><span class="sxs-lookup"><span data-stu-id="d1953-111">You can suppress this behavior using the Overwrite parameter, which updates the record set regardless of concurrent changes.</span></span>

## <span data-ttu-id="d1953-112">例子</span><span class="sxs-lookup"><span data-stu-id="d1953-112">EXAMPLES</span></span>

### <span data-ttu-id="d1953-113">範例 1：更新記錄集</span><span class="sxs-lookup"><span data-stu-id="d1953-113">Example 1: Update a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A
PS C:\> Add-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.16.0.0
PS C:\> Add-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.31.255.255
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# These cmdlets can also be piped:

PS C:\> Get-AzPrivateDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A | Add-AzPrivateDnsRecordConfig -Ipv4Address 172.16.0.0 | Add-AzPrivateDnsRecordConfig -Ipv4Address 172.31.255.255 | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.Netwo
                    rk/privateDnsZones/myzone.com/A/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {1.2.3.4, 172.16.0.0, 172.31.255.255}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="d1953-114">第一個命令使用 Get-AzPrivateDnsRecordSet Cmdlet 取得指定的記錄集，然後將它儲存在 $RecordSet 變數中。</span><span class="sxs-lookup"><span data-stu-id="d1953-114">The first command uses the Get-AzPrivateDnsRecordSet cmdlet to get the specified record set, and then stores it in the $RecordSet variable.</span></span> <span data-ttu-id="d1953-115">第二個和第三個命令是線下作業，在記錄集新增兩個 A 記錄。</span><span class="sxs-lookup"><span data-stu-id="d1953-115">The second and third commands are off-line operations to add two A records to the record set.</span></span> <span data-ttu-id="d1953-116">最後一個命令會使用 Set-AzPrivateDnsRecordSet Cmdlet 來提交更新。</span><span class="sxs-lookup"><span data-stu-id="d1953-116">The final command uses the Set-AzPrivateDnsRecordSet cmdlet to commit the update.</span></span>

### <span data-ttu-id="d1953-117">範例 2：更新一個</span><span class="sxs-lookup"><span data-stu-id="d1953-117">Example 2: Update an SOA record</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "@" -RecordType SOA -Zone $Zone
PS C:\> $RecordSet.Records[0].Email = "admin.myzone.com"
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/SOA/@
Name              : @
ZoneName          : myzone.com
ResourceGroupName : Myresourcegroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : SOA
Records           : {[internal.cloudapp.net,admin.myzone.com,3600,300,2419200,300]}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="d1953-118">第一個命令使用 Get-AzPrivateDnsRecordSet Cmdlet 取得指定的記錄集，然後將它儲存在 $RecordSet 變數中。</span><span class="sxs-lookup"><span data-stu-id="d1953-118">The first command uses the Get-AzPrivateDnsRecordSet cmdlet to get the specified record set, and then stores it in the $RecordSet variable.</span></span> <span data-ttu-id="d1953-119">第二個命令會更新 $RecordSet 中指定的 $RECORDSET。</span><span class="sxs-lookup"><span data-stu-id="d1953-119">The second command updates the specified SOA record in $RecordSet.</span></span> <span data-ttu-id="d1953-120">最後一個命令會使用 Set-AzPrivateDnsRecordSet Cmdlet 在 $RecordSet 中傳播$RecordSet。</span><span class="sxs-lookup"><span data-stu-id="d1953-120">The final command uses the Set-AzPrivateDnsRecordSet cmdlet to propagate the update in $RecordSet.</span></span>

## <span data-ttu-id="d1953-121">參數</span><span class="sxs-lookup"><span data-stu-id="d1953-121">PARAMETERS</span></span>

### <span data-ttu-id="d1953-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1953-122">-DefaultProfile</span></span>
<span data-ttu-id="d1953-123">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="d1953-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1953-124">-覆寫</span><span class="sxs-lookup"><span data-stu-id="d1953-124">-Overwrite</span></span>
<span data-ttu-id="d1953-125">請勿使用 RecordSet 參數的 ETag 欄位進行開放式並行檢查。</span><span class="sxs-lookup"><span data-stu-id="d1953-125">Do not use the ETag field of the RecordSet parameter for optimistic concurrency checks.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1953-126">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="d1953-126">-RecordSet</span></span>
<span data-ttu-id="d1953-127">要新增記錄的記錄集。</span><span class="sxs-lookup"><span data-stu-id="d1953-127">The record set in which to add the record.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d1953-128">-確認</span><span class="sxs-lookup"><span data-stu-id="d1953-128">-Confirm</span></span>
<span data-ttu-id="d1953-129">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="d1953-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1953-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1953-130">-WhatIf</span></span>
<span data-ttu-id="d1953-131">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d1953-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1953-132">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d1953-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1953-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1953-133">CommonParameters</span></span>
<span data-ttu-id="d1953-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d1953-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1953-135">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="d1953-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1953-136">輸入</span><span class="sxs-lookup"><span data-stu-id="d1953-136">INPUTS</span></span>

### <span data-ttu-id="d1953-137">Microsoft.Azure.Commands.PrivateDns.models.PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="d1953-137">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="d1953-138">輸出</span><span class="sxs-lookup"><span data-stu-id="d1953-138">OUTPUTS</span></span>

### <span data-ttu-id="d1953-139">Microsoft.Azure.Commands.PrivateDns.models.PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="d1953-139">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="d1953-140">筆記</span><span class="sxs-lookup"><span data-stu-id="d1953-140">NOTES</span></span>

## <span data-ttu-id="d1953-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="d1953-141">RELATED LINKS</span></span>
