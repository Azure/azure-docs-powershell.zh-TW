---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/Set-AzPrivateDnsRecordSet
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsRecordSet.md
ms.openlocfilehash: 7c4f76b9731e82bd134be7ae38461a7d74e31e6a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621210"
---
# <span data-ttu-id="798d8-101">Set-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="798d8-101">Set-AzPrivateDnsRecordSet</span></span>

## <span data-ttu-id="798d8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="798d8-102">SYNOPSIS</span></span>
<span data-ttu-id="798d8-103">更新/設定在私人 DNS 區域中設定的記錄。</span><span class="sxs-lookup"><span data-stu-id="798d8-103">Updates/Sets a record set in a Private DNS zone.</span></span>

## <span data-ttu-id="798d8-104">句法</span><span class="sxs-lookup"><span data-stu-id="798d8-104">SYNTAX</span></span>

```
Set-AzPrivateDnsRecordSet -RecordSet <PSPrivateDnsRecordSet> [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="798d8-105">說明</span><span class="sxs-lookup"><span data-stu-id="798d8-105">DESCRIPTION</span></span>
<span data-ttu-id="798d8-106">Set-AzPrivateDnsRecordSet Cmdlet 會從本機 RecordSet 物件更新 Azure 私人 DNS 服務中的記錄集。</span><span class="sxs-lookup"><span data-stu-id="798d8-106">The Set-AzPrivateDnsRecordSet cmdlet updates a record set in the Azure Private DNS service from a local RecordSet object.</span></span> <span data-ttu-id="798d8-107">您可以將 RecordSet 物件作為參數傳遞，或使用管線運算子。</span><span class="sxs-lookup"><span data-stu-id="798d8-107">You can pass a RecordSet object as a parameter or by using the pipeline operator.</span></span> <span data-ttu-id="798d8-108">您可以使用 Confirm 參數和 $ConfirmPreference 的 Windows PowerShell 變數來控制 Cmdlet 是否提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="798d8-108">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span> <span data-ttu-id="798d8-109">如果在已檢索到本機 RecordSet 物件之後，在 Azure 私人 DNS 中變更記錄集，則不會更新。</span><span class="sxs-lookup"><span data-stu-id="798d8-109">The record set is not updated if it has been changed in Azure Private DNS since the local RecordSet object was retrieved.</span></span> <span data-ttu-id="798d8-110">這可為併發變更提供保護。</span><span class="sxs-lookup"><span data-stu-id="798d8-110">This provides protection for concurrent changes.</span></span> <span data-ttu-id="798d8-111">您可以使用 Overwrite 參數來隱含此行為，不論併發變更為何，都會更新記錄集。</span><span class="sxs-lookup"><span data-stu-id="798d8-111">You can suppress this behavior using the Overwrite parameter, which updates the record set regardless of concurrent changes.</span></span>

## <span data-ttu-id="798d8-112">示例</span><span class="sxs-lookup"><span data-stu-id="798d8-112">EXAMPLES</span></span>

### <span data-ttu-id="798d8-113">範例1：更新記錄集</span><span class="sxs-lookup"><span data-stu-id="798d8-113">Example 1: Update a record set</span></span>
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

<span data-ttu-id="798d8-114">第一個命令使用 Get-AzPrivateDnsRecordSet Cmdlet 來取得指定的記錄集，然後將它儲存在 $RecordSet 變數中。</span><span class="sxs-lookup"><span data-stu-id="798d8-114">The first command uses the Get-AzPrivateDnsRecordSet cmdlet to get the specified record set, and then stores it in the $RecordSet variable.</span></span> <span data-ttu-id="798d8-115">第二個和第三個命令是離線作業，可將兩筆記錄新增至記錄集。</span><span class="sxs-lookup"><span data-stu-id="798d8-115">The second and third commands are off-line operations to add two A records to the record set.</span></span> <span data-ttu-id="798d8-116">Final 命令會使用 Set-AzPrivateDnsRecordSet Cmdlet 來認可更新。</span><span class="sxs-lookup"><span data-stu-id="798d8-116">The final command uses the Set-AzPrivateDnsRecordSet cmdlet to commit the update.</span></span>

### <span data-ttu-id="798d8-117">範例2：更新 SOA 記錄</span><span class="sxs-lookup"><span data-stu-id="798d8-117">Example 2: Update an SOA record</span></span>
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

<span data-ttu-id="798d8-118">第一個命令使用 Get-AzPrivateDnsRecordSet Cmdlet 來取得指定的記錄集，然後將它儲存在 $RecordSet 變數中。</span><span class="sxs-lookup"><span data-stu-id="798d8-118">The first command uses the Get-AzPrivateDnsRecordSet cmdlet to get the specified record set, and then stores it in the $RecordSet variable.</span></span> <span data-ttu-id="798d8-119">第二個命令會更新 $RecordSet 中指定的 SOA 記錄。</span><span class="sxs-lookup"><span data-stu-id="798d8-119">The second command updates the specified SOA record in $RecordSet.</span></span> <span data-ttu-id="798d8-120">Final 命令會使用 Set-AzPrivateDnsRecordSet Cmdlet 來傳播 $RecordSet 中的更新。</span><span class="sxs-lookup"><span data-stu-id="798d8-120">The final command uses the Set-AzPrivateDnsRecordSet cmdlet to propagate the update in $RecordSet.</span></span>

## <span data-ttu-id="798d8-121">參數</span><span class="sxs-lookup"><span data-stu-id="798d8-121">PARAMETERS</span></span>

### <span data-ttu-id="798d8-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="798d8-122">-DefaultProfile</span></span>
<span data-ttu-id="798d8-123">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="798d8-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="798d8-124">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="798d8-124">-Overwrite</span></span>
<span data-ttu-id="798d8-125">請勿使用 RecordSet 參數的 ETag 欄位來進行開放式併發檢查。</span><span class="sxs-lookup"><span data-stu-id="798d8-125">Do not use the ETag field of the RecordSet parameter for optimistic concurrency checks.</span></span>

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

### <span data-ttu-id="798d8-126">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="798d8-126">-RecordSet</span></span>
<span data-ttu-id="798d8-127">要在其中新增記錄的記錄集。</span><span class="sxs-lookup"><span data-stu-id="798d8-127">The record set in which to add the record.</span></span>

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

### <span data-ttu-id="798d8-128">-確認</span><span class="sxs-lookup"><span data-stu-id="798d8-128">-Confirm</span></span>
<span data-ttu-id="798d8-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="798d8-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="798d8-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="798d8-130">-WhatIf</span></span>
<span data-ttu-id="798d8-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="798d8-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="798d8-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="798d8-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="798d8-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="798d8-133">CommonParameters</span></span>
<span data-ttu-id="798d8-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="798d8-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="798d8-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="798d8-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="798d8-136">輸入</span><span class="sxs-lookup"><span data-stu-id="798d8-136">INPUTS</span></span>

### <span data-ttu-id="798d8-137">PSPrivateDnsRecordSet 中的 PrivateDns。</span><span class="sxs-lookup"><span data-stu-id="798d8-137">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="798d8-138">輸出</span><span class="sxs-lookup"><span data-stu-id="798d8-138">OUTPUTS</span></span>

### <span data-ttu-id="798d8-139">PSPrivateDnsRecordSet 中的 PrivateDns。</span><span class="sxs-lookup"><span data-stu-id="798d8-139">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="798d8-140">筆記</span><span class="sxs-lookup"><span data-stu-id="798d8-140">NOTES</span></span>

## <span data-ttu-id="798d8-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="798d8-141">RELATED LINKS</span></span>
