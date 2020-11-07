---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 99E6C4DD-11AF-4DC0-848B-39811240BE06
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/set-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Set-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Set-AzDnsRecordSet.md
ms.openlocfilehash: e75d394596b85c75dc79b0eb0d2b19525aa9c7c4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93956889"
---
# <span data-ttu-id="c240d-101">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="c240d-101">Set-AzDnsRecordSet</span></span>

## <span data-ttu-id="c240d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c240d-102">SYNOPSIS</span></span>
<span data-ttu-id="c240d-103">更新 DNS 記錄集。</span><span class="sxs-lookup"><span data-stu-id="c240d-103">Updates a DNS record set.</span></span>

## <span data-ttu-id="c240d-104">句法</span><span class="sxs-lookup"><span data-stu-id="c240d-104">SYNTAX</span></span>

```
Set-AzDnsRecordSet -RecordSet <DnsRecordSet> [-Overwrite] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c240d-105">說明</span><span class="sxs-lookup"><span data-stu-id="c240d-105">DESCRIPTION</span></span>
<span data-ttu-id="c240d-106">**AzDnsRecordSet** Cmdlet 會從本機 **RecordSet** 物件更新 Azure DNS 服務中的記錄集。</span><span class="sxs-lookup"><span data-stu-id="c240d-106">The **Set-AzDnsRecordSet** cmdlet updates a record set in the Azure DNS service from a local **RecordSet** object.</span></span>
<span data-ttu-id="c240d-107">您可以將 **RecordSet** 物件作為參數傳遞，或使用管線運算子。</span><span class="sxs-lookup"><span data-stu-id="c240d-107">You can pass a **RecordSet** object as a parameter or by using the pipeline operator.</span></span>
<span data-ttu-id="c240d-108">您可以使用 *Confirm* 參數和 $ConfirmPreference 的 Windows PowerShell 變數來控制 Cmdlet 是否提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c240d-108">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="c240d-109">如果自檢索到本機 **RecordSet** 物件之後，在 Azure DNS 中變更記錄集，則不會更新。</span><span class="sxs-lookup"><span data-stu-id="c240d-109">The record set is not updated if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="c240d-110">這可為併發變更提供保護。</span><span class="sxs-lookup"><span data-stu-id="c240d-110">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="c240d-111">您可以使用 *Overwrite* 參數來隱含此行為，不論併發變更為何，都會更新記錄集。</span><span class="sxs-lookup"><span data-stu-id="c240d-111">You can suppress this behavior using the *Overwrite* parameter, which updates the record set regardless of concurrent changes.</span></span>

## <span data-ttu-id="c240d-112">示例</span><span class="sxs-lookup"><span data-stu-id="c240d-112">EXAMPLES</span></span>

### <span data-ttu-id="c240d-113">範例1：更新記錄集</span><span class="sxs-lookup"><span data-stu-id="c240d-113">Example 1: Update a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.16.0.0
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.31.255.255
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# These cmdlets can also be piped:

PS C:\> Get-AzDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A | Add-AzDnsRecordConfig -Ipv4Address 172.16.0.0 | Add-AzDnsRecordConfig -Ipv4Address 172.31.255.255 | Set-AzDnsRecordSet
```

<span data-ttu-id="c240d-114">第一個命令使用 Get-AzDnsRecordSet Cmdlet 來取得指定的記錄集，然後將它儲存在 $RecordSet 變數中。</span><span class="sxs-lookup"><span data-stu-id="c240d-114">The first command uses the Get-AzDnsRecordSet cmdlet to get the specified record set, and then stores it in the $RecordSet variable.</span></span>
<span data-ttu-id="c240d-115">第二個和第三個命令是離線作業，可將兩筆記錄新增至記錄集。</span><span class="sxs-lookup"><span data-stu-id="c240d-115">The second and third commands are off-line operations to add two A records to the record set.</span></span>
<span data-ttu-id="c240d-116">最終命令會使用 **AzDnsRecordSet** Cmdlet 來認可更新。</span><span class="sxs-lookup"><span data-stu-id="c240d-116">The final command uses the **Set-AzDnsRecordSet** cmdlet to commit the update.</span></span>

### <span data-ttu-id="c240d-117">範例2：更新 SOA 記錄</span><span class="sxs-lookup"><span data-stu-id="c240d-117">Example 2: Update an SOA record</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name "@" -RecordType SOA -Zone $Zone
PS C:\> $RecordSet.Records[0].Email = "admin.myzone.com"
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet
```

<span data-ttu-id="c240d-118">第一個命令使用 **AzDnsRecordset** Cmdlet 來取得指定的記錄集，然後將它儲存在 $RecordSet 變數中。</span><span class="sxs-lookup"><span data-stu-id="c240d-118">The first command uses the **Get-AzDnsRecordset** cmdlet to get the specified record set, and then stores it in the $RecordSet variable.</span></span>
<span data-ttu-id="c240d-119">第二個命令會更新 $RecordSet 中指定的 SOA 記錄。</span><span class="sxs-lookup"><span data-stu-id="c240d-119">The second command updates the specified SOA record in $RecordSet.</span></span>
<span data-ttu-id="c240d-120">Final 命令會使用 **AzDnsRecordSet** Cmdlet 來傳播 $RecordSet 中的更新。</span><span class="sxs-lookup"><span data-stu-id="c240d-120">The final command uses the **Set-AzDnsRecordSet** cmdlet to propagate the update in $RecordSet.</span></span>

## <span data-ttu-id="c240d-121">參數</span><span class="sxs-lookup"><span data-stu-id="c240d-121">PARAMETERS</span></span>

### <span data-ttu-id="c240d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c240d-122">-DefaultProfile</span></span>
<span data-ttu-id="c240d-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="c240d-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c240d-124">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="c240d-124">-Overwrite</span></span>
<span data-ttu-id="c240d-125">指示更新記錄集（不論併發變更）。</span><span class="sxs-lookup"><span data-stu-id="c240d-125">Indicates to update the record set regardless of concurrent changes.</span></span>
<span data-ttu-id="c240d-126">如果自檢索到本機 **RecordSet** 物件之後，在 Azure DNS 中變更記錄集，則不會更新。</span><span class="sxs-lookup"><span data-stu-id="c240d-126">The record set will not be updated if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="c240d-127">這可為併發變更提供保護。</span><span class="sxs-lookup"><span data-stu-id="c240d-127">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="c240d-128">若要取消此行為，您可以使用 *Overwrite* 參數，不論併發變更為何，都會更新記錄集合。</span><span class="sxs-lookup"><span data-stu-id="c240d-128">To suppress this behavior, you can use the *Overwrite* parameter, which results in the record set being updated regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="c240d-129">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="c240d-129">-RecordSet</span></span>
<span data-ttu-id="c240d-130">指定要更新的 **記錄集** 。</span><span class="sxs-lookup"><span data-stu-id="c240d-130">Specifies the **RecordSet** to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsRecordSet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c240d-131">-確認</span><span class="sxs-lookup"><span data-stu-id="c240d-131">-Confirm</span></span>
<span data-ttu-id="c240d-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c240d-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c240d-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c240d-133">-WhatIf</span></span>
<span data-ttu-id="c240d-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c240d-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c240d-135">未執行 Cmdlet。顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c240d-135">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c240d-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c240d-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c240d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c240d-137">CommonParameters</span></span>
<span data-ttu-id="c240d-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c240d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c240d-139">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c240d-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c240d-140">輸入</span><span class="sxs-lookup"><span data-stu-id="c240d-140">INPUTS</span></span>

### <span data-ttu-id="c240d-141">DnsRecordSet （）</span><span class="sxs-lookup"><span data-stu-id="c240d-141">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="c240d-142">輸出</span><span class="sxs-lookup"><span data-stu-id="c240d-142">OUTPUTS</span></span>

### <span data-ttu-id="c240d-143">DnsRecordSet （）</span><span class="sxs-lookup"><span data-stu-id="c240d-143">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="c240d-144">筆記</span><span class="sxs-lookup"><span data-stu-id="c240d-144">NOTES</span></span>
<span data-ttu-id="c240d-145">您可以使用 *Confirm* 參數來控制此 Cmdlet 是否提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c240d-145">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="c240d-146">根據預設，如果 $ConfirmPreference 的 Windows PowerShell 變數的值為 [中] 或 [低]，則該 Cmdlet 會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c240d-146">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>
<span data-ttu-id="c240d-147">如果您指定 [ *確認* ] 或 [ *確認]： $True* ，此 Cmdlet 會在您執行之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c240d-147">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="c240d-148">如果您指定 [ *確認： $False* ]，則 Cmdlet 不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c240d-148">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span> 

## <span data-ttu-id="c240d-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="c240d-149">RELATED LINKS</span></span>

[<span data-ttu-id="c240d-150">AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="c240d-150">Get-AzDnsRecordSet</span></span>](./Get-AzDnsRecordSet.md)

[<span data-ttu-id="c240d-151">新-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="c240d-151">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="c240d-152">移除-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="c240d-152">Remove-AzDnsRecordSet</span></span>](./Remove-AzDnsRecordSet.md)
