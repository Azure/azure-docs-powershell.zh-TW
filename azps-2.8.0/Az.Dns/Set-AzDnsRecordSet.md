---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 99E6C4DD-11AF-4DC0-848B-39811240BE06
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/set-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Set-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Set-AzDnsRecordSet.md
ms.openlocfilehash: c57377156acbf908825638e13f139114fa5d811c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93612487"
---
# <span data-ttu-id="581f6-101">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="581f6-101">Set-AzDnsRecordSet</span></span>

## <span data-ttu-id="581f6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="581f6-102">SYNOPSIS</span></span>
<span data-ttu-id="581f6-103">更新 DNS 記錄集。</span><span class="sxs-lookup"><span data-stu-id="581f6-103">Updates a DNS record set.</span></span>

## <span data-ttu-id="581f6-104">句法</span><span class="sxs-lookup"><span data-stu-id="581f6-104">SYNTAX</span></span>

```
Set-AzDnsRecordSet -RecordSet <DnsRecordSet> [-Overwrite] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="581f6-105">說明</span><span class="sxs-lookup"><span data-stu-id="581f6-105">DESCRIPTION</span></span>
<span data-ttu-id="581f6-106">**AzDnsRecordSet** Cmdlet 會從本機 **RecordSet** 物件更新 Azure DNS 服務中的記錄集。</span><span class="sxs-lookup"><span data-stu-id="581f6-106">The **Set-AzDnsRecordSet** cmdlet updates a record set in the Azure DNS service from a local **RecordSet** object.</span></span>
<span data-ttu-id="581f6-107">您可以將 **RecordSet** 物件作為參數傳遞，或使用管線運算子。</span><span class="sxs-lookup"><span data-stu-id="581f6-107">You can pass a **RecordSet** object as a parameter or by using the pipeline operator.</span></span>
<span data-ttu-id="581f6-108">您可以使用 *Confirm* 參數和 $ConfirmPreference 的 Windows PowerShell 變數來控制 Cmdlet 是否提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="581f6-108">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="581f6-109">如果自檢索到本機 **RecordSet** 物件之後，在 Azure DNS 中變更記錄集，則不會更新。</span><span class="sxs-lookup"><span data-stu-id="581f6-109">The record set is not updated if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="581f6-110">這可為併發變更提供保護。</span><span class="sxs-lookup"><span data-stu-id="581f6-110">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="581f6-111">您可以使用 *Overwrite* 參數來隱含此行為，不論併發變更為何，都會更新記錄集。</span><span class="sxs-lookup"><span data-stu-id="581f6-111">You can suppress this behavior using the *Overwrite* parameter, which updates the record set regardless of concurrent changes.</span></span>

## <span data-ttu-id="581f6-112">示例</span><span class="sxs-lookup"><span data-stu-id="581f6-112">EXAMPLES</span></span>

### <span data-ttu-id="581f6-113">範例1：更新記錄集</span><span class="sxs-lookup"><span data-stu-id="581f6-113">Example 1: Update a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.16.0.0
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.31.255.255
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# These cmdlets can also be piped:

PS C:\> Get-AzDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A | Add-AzDnsRecordConfig -Ipv4Address 172.16.0.0 | Add-AzDnsRecordConfig -Ipv4Address 172.31.255.255 | Set-AzDnsRecordSet
```

<span data-ttu-id="581f6-114">第一個命令使用 Get-AzDnsRecordSet Cmdlet 來取得指定的記錄集，然後將它儲存在 $RecordSet 變數中。</span><span class="sxs-lookup"><span data-stu-id="581f6-114">The first command uses the Get-AzDnsRecordSet cmdlet to get the specified record set, and then stores it in the $RecordSet variable.</span></span>
<span data-ttu-id="581f6-115">第二個和第三個命令是離線作業，可將兩筆記錄新增至記錄集。</span><span class="sxs-lookup"><span data-stu-id="581f6-115">The second and third commands are off-line operations to add two A records to the record set.</span></span>
<span data-ttu-id="581f6-116">最終命令會使用 **AzDnsRecordSet** Cmdlet 來認可更新。</span><span class="sxs-lookup"><span data-stu-id="581f6-116">The final command uses the **Set-AzDnsRecordSet** cmdlet to commit the update.</span></span>

### <span data-ttu-id="581f6-117">範例2：更新 SOA 記錄</span><span class="sxs-lookup"><span data-stu-id="581f6-117">Example 2: Update an SOA record</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name "@" -RecordType SOA -Zone $Zone
PS C:\> $RecordSet.Records[0].Email = "admin.myzone.com"
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet
```

<span data-ttu-id="581f6-118">第一個命令使用 **AzDnsRecordset** Cmdlet 來取得指定的記錄集，然後將它儲存在 $RecordSet 變數中。</span><span class="sxs-lookup"><span data-stu-id="581f6-118">The first command uses the **Get-AzDnsRecordset** cmdlet to get the specified record set, and then stores it in the $RecordSet variable.</span></span>
<span data-ttu-id="581f6-119">第二個命令會更新 $RecordSet 中指定的 SOA 記錄。</span><span class="sxs-lookup"><span data-stu-id="581f6-119">The second command updates the specified SOA record in $RecordSet.</span></span>
<span data-ttu-id="581f6-120">Final 命令會使用 **AzDnsRecordSet** Cmdlet 來傳播 $RecordSet 中的更新。</span><span class="sxs-lookup"><span data-stu-id="581f6-120">The final command uses the **Set-AzDnsRecordSet** cmdlet to propagate the update in $RecordSet.</span></span>

## <span data-ttu-id="581f6-121">參數</span><span class="sxs-lookup"><span data-stu-id="581f6-121">PARAMETERS</span></span>

### <span data-ttu-id="581f6-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="581f6-122">-DefaultProfile</span></span>
<span data-ttu-id="581f6-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="581f6-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="581f6-124">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="581f6-124">-Overwrite</span></span>
<span data-ttu-id="581f6-125">指示更新記錄集（不論併發變更）。</span><span class="sxs-lookup"><span data-stu-id="581f6-125">Indicates to update the record set regardless of concurrent changes.</span></span>
<span data-ttu-id="581f6-126">如果自檢索到本機 **RecordSet** 物件之後，在 Azure DNS 中變更記錄集，則不會更新。</span><span class="sxs-lookup"><span data-stu-id="581f6-126">The record set will not be updated if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="581f6-127">這可為併發變更提供保護。</span><span class="sxs-lookup"><span data-stu-id="581f6-127">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="581f6-128">若要取消此行為，您可以使用 *Overwrite* 參數，不論併發變更為何，都會更新記錄集合。</span><span class="sxs-lookup"><span data-stu-id="581f6-128">To suppress this behavior, you can use the *Overwrite* parameter, which results in the record set being updated regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="581f6-129">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="581f6-129">-RecordSet</span></span>
<span data-ttu-id="581f6-130">指定要更新的 **記錄集** 。</span><span class="sxs-lookup"><span data-stu-id="581f6-130">Specifies the **RecordSet** to update.</span></span>

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

### <span data-ttu-id="581f6-131">-確認</span><span class="sxs-lookup"><span data-stu-id="581f6-131">-Confirm</span></span>
<span data-ttu-id="581f6-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="581f6-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="581f6-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="581f6-133">-WhatIf</span></span>
<span data-ttu-id="581f6-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="581f6-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="581f6-135">未執行 Cmdlet。顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="581f6-135">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="581f6-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="581f6-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="581f6-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="581f6-137">CommonParameters</span></span>
<span data-ttu-id="581f6-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="581f6-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="581f6-139">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="581f6-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="581f6-140">輸入</span><span class="sxs-lookup"><span data-stu-id="581f6-140">INPUTS</span></span>

### <span data-ttu-id="581f6-141">DnsRecordSet （）</span><span class="sxs-lookup"><span data-stu-id="581f6-141">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="581f6-142">輸出</span><span class="sxs-lookup"><span data-stu-id="581f6-142">OUTPUTS</span></span>

### <span data-ttu-id="581f6-143">DnsRecordSet （）</span><span class="sxs-lookup"><span data-stu-id="581f6-143">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="581f6-144">筆記</span><span class="sxs-lookup"><span data-stu-id="581f6-144">NOTES</span></span>
<span data-ttu-id="581f6-145">您可以使用 *Confirm* 參數來控制此 Cmdlet 是否提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="581f6-145">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="581f6-146">根據預設，如果 $ConfirmPreference 的 Windows PowerShell 變數的值為 [中] 或 [低]，則該 Cmdlet 會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="581f6-146">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>
<span data-ttu-id="581f6-147">如果您指定 [ *確認* ] 或 [ *確認]： $True* ，此 Cmdlet 會在您執行之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="581f6-147">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="581f6-148">如果您指定 [ *確認： $False* ]，則 Cmdlet 不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="581f6-148">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span> 

## <span data-ttu-id="581f6-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="581f6-149">RELATED LINKS</span></span>

[<span data-ttu-id="581f6-150">AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="581f6-150">Get-AzDnsRecordSet</span></span>](./Get-AzDnsRecordSet.md)

[<span data-ttu-id="581f6-151">新-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="581f6-151">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="581f6-152">移除-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="581f6-152">Remove-AzDnsRecordSet</span></span>](./Remove-AzDnsRecordSet.md)