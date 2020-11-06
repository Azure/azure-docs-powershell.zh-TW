---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: 99E6C4DD-11AF-4DC0-848B-39811240BE06
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.dns/set-azurermdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Set-AzureRmDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Set-AzureRmDnsRecordSet.md
ms.openlocfilehash: d0a7451db664d80240250984fcc1c0f8e1aaefe9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451179"
---
# <span data-ttu-id="efea4-101">Set-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="efea4-101">Set-AzureRmDnsRecordSet</span></span>

## <span data-ttu-id="efea4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="efea4-102">SYNOPSIS</span></span>
<span data-ttu-id="efea4-103">更新 DNS 記錄集。</span><span class="sxs-lookup"><span data-stu-id="efea4-103">Updates a DNS record set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="efea4-104">句法</span><span class="sxs-lookup"><span data-stu-id="efea4-104">SYNTAX</span></span>

```
Set-AzureRmDnsRecordSet -RecordSet <DnsRecordSet> [-Overwrite] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="efea4-105">說明</span><span class="sxs-lookup"><span data-stu-id="efea4-105">DESCRIPTION</span></span>
<span data-ttu-id="efea4-106">**AzureRmDnsRecordSet** Cmdlet 會從本機 **RecordSet** 物件更新 Azure DNS 服務中的記錄集。</span><span class="sxs-lookup"><span data-stu-id="efea4-106">The **Set-AzureRmDnsRecordSet** cmdlet updates a record set in the Azure DNS service from a local **RecordSet** object.</span></span>
<span data-ttu-id="efea4-107">您可以將 **RecordSet** 物件作為參數傳遞，或使用管線運算子。</span><span class="sxs-lookup"><span data-stu-id="efea4-107">You can pass a **RecordSet** object as a parameter or by using the pipeline operator.</span></span>
<span data-ttu-id="efea4-108">您可以使用 *Confirm* 參數和 $ConfirmPreference 的 Windows PowerShell 變數來控制 Cmdlet 是否提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="efea4-108">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="efea4-109">如果自檢索到本機 **RecordSet** 物件之後，在 Azure DNS 中變更記錄集，則不會更新。</span><span class="sxs-lookup"><span data-stu-id="efea4-109">The record set is not updated if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="efea4-110">這可為併發變更提供保護。</span><span class="sxs-lookup"><span data-stu-id="efea4-110">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="efea4-111">您可以使用 *Overwrite* 參數來隱含此行為，不論併發變更為何，都會更新記錄集。</span><span class="sxs-lookup"><span data-stu-id="efea4-111">You can suppress this behavior using the *Overwrite* parameter, which updates the record set regardless of concurrent changes.</span></span>

## <span data-ttu-id="efea4-112">示例</span><span class="sxs-lookup"><span data-stu-id="efea4-112">EXAMPLES</span></span>

### <span data-ttu-id="efea4-113">範例1：更新記錄集</span><span class="sxs-lookup"><span data-stu-id="efea4-113">Example 1: Update a record set</span></span>
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A
PS C:\> Add-AzureRmDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.16.0.0
PS C:\> Add-AzureRmDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.31.255.255
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# These cmdlets can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A | Add-AzureRmDnsRecordConfig -Ipv4Address 172.16.0.0 | Add-AzureRmDnsRecordConfig -Ipv4Address 172.31.255.255 | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="efea4-114">第一個命令使用 Get-AzureRmDnsRecordSet Cmdlet 來取得指定的記錄集，然後將它儲存在 $RecordSet 變數中。</span><span class="sxs-lookup"><span data-stu-id="efea4-114">The first command uses the Get-AzureRmDnsRecordSet cmdlet to get the specified record set, and then stores it in the $RecordSet variable.</span></span>
<span data-ttu-id="efea4-115">第二個和第三個命令是離線作業，可將兩筆記錄新增至記錄集。</span><span class="sxs-lookup"><span data-stu-id="efea4-115">The second and third commands are off-line operations to add two A records to the record set.</span></span>
<span data-ttu-id="efea4-116">最終命令會使用 **AzureRmDnsRecordSet** Cmdlet 來認可更新。</span><span class="sxs-lookup"><span data-stu-id="efea4-116">The final command uses the **Set-AzureRmDnsRecordSet** cmdlet to commit the update.</span></span>

### <span data-ttu-id="efea4-117">範例2：更新 SOA 記錄</span><span class="sxs-lookup"><span data-stu-id="efea4-117">Example 2: Update an SOA record</span></span>
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -Name "@" -RecordType SOA -Zone $Zone
PS C:\> $RecordSet.Records[0].Email = "admin.myzone.com"
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet
```

<span data-ttu-id="efea4-118">第一個命令使用 **AzureRmDnsRecordset** Cmdlet 來取得指定的記錄集，然後將它儲存在 $RecordSet 變數中。</span><span class="sxs-lookup"><span data-stu-id="efea4-118">The first command uses the **Get-AzureRmDnsRecordset** cmdlet to get the specified record set, and then stores it in the $RecordSet variable.</span></span>
<span data-ttu-id="efea4-119">第二個命令會更新 $RecordSet 中指定的 SOA 記錄。</span><span class="sxs-lookup"><span data-stu-id="efea4-119">The second command updates the specified SOA record in $RecordSet.</span></span>
<span data-ttu-id="efea4-120">Final 命令會使用 **AzureRmDnsRecordSet** Cmdlet 來傳播 $RecordSet 中的更新。</span><span class="sxs-lookup"><span data-stu-id="efea4-120">The final command uses the **Set-AzureRmDnsRecordSet** cmdlet to propagate the update in $RecordSet.</span></span>

## <span data-ttu-id="efea4-121">參數</span><span class="sxs-lookup"><span data-stu-id="efea4-121">PARAMETERS</span></span>

### <span data-ttu-id="efea4-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efea4-122">-DefaultProfile</span></span>
<span data-ttu-id="efea4-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="efea4-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efea4-124">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="efea4-124">-Overwrite</span></span>
<span data-ttu-id="efea4-125">指示更新記錄集（不論併發變更）。</span><span class="sxs-lookup"><span data-stu-id="efea4-125">Indicates to update the record set regardless of concurrent changes.</span></span>
<span data-ttu-id="efea4-126">如果自檢索到本機 **RecordSet** 物件之後，在 Azure DNS 中變更記錄集，則不會更新。</span><span class="sxs-lookup"><span data-stu-id="efea4-126">The record set will not be updated if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="efea4-127">這可為併發變更提供保護。</span><span class="sxs-lookup"><span data-stu-id="efea4-127">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="efea4-128">若要取消此行為，您可以使用 *Overwrite* 參數，不論併發變更為何，都會更新記錄集合。</span><span class="sxs-lookup"><span data-stu-id="efea4-128">To suppress this behavior, you can use the *Overwrite* parameter, which results in the record set being updated regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="efea4-129">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="efea4-129">-RecordSet</span></span>
<span data-ttu-id="efea4-130">指定要更新的 **記錄集** 。</span><span class="sxs-lookup"><span data-stu-id="efea4-130">Specifies the **RecordSet** to update.</span></span>

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

### <span data-ttu-id="efea4-131">-確認</span><span class="sxs-lookup"><span data-stu-id="efea4-131">-Confirm</span></span>
<span data-ttu-id="efea4-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="efea4-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="efea4-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="efea4-133">-WhatIf</span></span>
<span data-ttu-id="efea4-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="efea4-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="efea4-135">未執行 Cmdlet。顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="efea4-135">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="efea4-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="efea4-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="efea4-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efea4-137">CommonParameters</span></span>
<span data-ttu-id="efea4-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="efea4-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efea4-139">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="efea4-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efea4-140">輸入</span><span class="sxs-lookup"><span data-stu-id="efea4-140">INPUTS</span></span>

### <span data-ttu-id="efea4-141">DnsRecordSet （）</span><span class="sxs-lookup"><span data-stu-id="efea4-141">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="efea4-142">參數： RecordSet (ByValue) </span><span class="sxs-lookup"><span data-stu-id="efea4-142">Parameters: RecordSet (ByValue)</span></span>

## <span data-ttu-id="efea4-143">輸出</span><span class="sxs-lookup"><span data-stu-id="efea4-143">OUTPUTS</span></span>

### <span data-ttu-id="efea4-144">DnsRecordSet （）</span><span class="sxs-lookup"><span data-stu-id="efea4-144">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="efea4-145">筆記</span><span class="sxs-lookup"><span data-stu-id="efea4-145">NOTES</span></span>
<span data-ttu-id="efea4-146">您可以使用 *Confirm* 參數來控制此 Cmdlet 是否提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="efea4-146">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="efea4-147">根據預設，如果 $ConfirmPreference 的 Windows PowerShell 變數的值為 [中] 或 [低]，則該 Cmdlet 會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="efea4-147">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>
<span data-ttu-id="efea4-148">如果您指定 [ *確認* ] 或 [ *確認]： $True* ，此 Cmdlet 會在您執行之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="efea4-148">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="efea4-149">如果您指定 [ *確認： $False* ]，則 Cmdlet 不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="efea4-149">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span> 

## <span data-ttu-id="efea4-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="efea4-150">RELATED LINKS</span></span>

[<span data-ttu-id="efea4-151">AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="efea4-151">Get-AzureRmDnsRecordSet</span></span>](./Get-AzureRmDnsRecordSet.md)

[<span data-ttu-id="efea4-152">新-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="efea4-152">New-AzureRmDnsRecordSet</span></span>](./New-AzureRmDnsRecordSet.md)

[<span data-ttu-id="efea4-153">移除-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="efea4-153">Remove-AzureRmDnsRecordSet</span></span>](./Remove-AzureRmDnsRecordSet.md)
