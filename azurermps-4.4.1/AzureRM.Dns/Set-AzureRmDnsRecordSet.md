---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: 99E6C4DD-11AF-4DC0-848B-39811240BE06
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Set-AzureRmDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Set-AzureRmDnsRecordSet.md
ms.openlocfilehash: 9db3efc71b751f291c5bb8636246ed6927200c37
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446814"
---
# <span data-ttu-id="da4cd-101">Set-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="da4cd-101">Set-AzureRmDnsRecordSet</span></span>

## <span data-ttu-id="da4cd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="da4cd-102">SYNOPSIS</span></span>
<span data-ttu-id="da4cd-103">更新 DNS 記錄集。</span><span class="sxs-lookup"><span data-stu-id="da4cd-103">Updates a DNS record set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="da4cd-104">句法</span><span class="sxs-lookup"><span data-stu-id="da4cd-104">SYNTAX</span></span>

```
Set-AzureRmDnsRecordSet -RecordSet <DnsRecordSet> [-Overwrite] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da4cd-105">說明</span><span class="sxs-lookup"><span data-stu-id="da4cd-105">DESCRIPTION</span></span>
<span data-ttu-id="da4cd-106">**AzureRmDnsRecordSet** Cmdlet 會從本機 **RecordSet** 物件更新 Azure DNS 服務中的記錄集。</span><span class="sxs-lookup"><span data-stu-id="da4cd-106">The **Set-AzureRmDnsRecordSet** cmdlet updates a record set in the Azure DNS service from a local **RecordSet** object.</span></span>

<span data-ttu-id="da4cd-107">您可以將 **RecordSet** 物件作為參數傳遞，或使用管線運算子。</span><span class="sxs-lookup"><span data-stu-id="da4cd-107">You can pass a **RecordSet** object as a parameter or by using the pipeline operator.</span></span>

<span data-ttu-id="da4cd-108">您可以使用 *Confirm* 參數和 $ConfirmPreference 的 Windows PowerShell 變數來控制 Cmdlet 是否提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="da4cd-108">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

<span data-ttu-id="da4cd-109">如果自檢索到本機 **RecordSet** 物件之後，在 Azure DNS 中變更記錄集，則不會更新。</span><span class="sxs-lookup"><span data-stu-id="da4cd-109">The record set is not updated if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="da4cd-110">這可為併發變更提供保護。</span><span class="sxs-lookup"><span data-stu-id="da4cd-110">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="da4cd-111">您可以使用 *Overwrite* 參數來隱含此行為，不論併發變更為何，都會更新記錄集。</span><span class="sxs-lookup"><span data-stu-id="da4cd-111">You can suppress this behavior using the *Overwrite* parameter, which updates the record set regardless of concurrent changes.</span></span>

## <span data-ttu-id="da4cd-112">示例</span><span class="sxs-lookup"><span data-stu-id="da4cd-112">EXAMPLES</span></span>

### <span data-ttu-id="da4cd-113">範例1：更新記錄集</span><span class="sxs-lookup"><span data-stu-id="da4cd-113">Example 1: Update a record set</span></span>
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A
PS C:\> Add-AzureRmDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.16.0.0
PS C:\> Add-AzureRmDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.31.255.255
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# These cmdlets can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A | Add-AzureRmDnsRecordConfig -Ipv4Address 172.16.0.0 | Add-AzureRmDnsRecordConfig -Ipv4Address 172.31.255.255 | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="da4cd-114">第一個命令使用 Get-AzureRmDnsRecordSet Cmdlet 來取得指定的記錄集，然後將它儲存在 $RecordSet 變數中。</span><span class="sxs-lookup"><span data-stu-id="da4cd-114">The first command uses the Get-AzureRmDnsRecordSet cmdlet to get the specified record set, and then stores it in the $RecordSet variable.</span></span>

<span data-ttu-id="da4cd-115">第二個和第三個命令是離線作業，可將兩筆記錄新增至記錄集。</span><span class="sxs-lookup"><span data-stu-id="da4cd-115">The second and third commands are off-line operations to add two A records to the record set.</span></span>

<span data-ttu-id="da4cd-116">最終命令會使用 **AzureRmDnsRecordSet** Cmdlet 來認可更新。</span><span class="sxs-lookup"><span data-stu-id="da4cd-116">The final command uses the **Set-AzureRmDnsRecordSet** cmdlet to commit the update.</span></span>

### <span data-ttu-id="da4cd-117">範例2：更新 SOA 記錄</span><span class="sxs-lookup"><span data-stu-id="da4cd-117">Example 2: Update an SOA record</span></span>
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -Name "@" -RecordType SOA -Zone $Zone
PS C:\> $RecordSet.Records[0].Email = "admin.myzone.com"
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet
```

<span data-ttu-id="da4cd-118">第一個命令使用 **AzureRmDnsRecordset** Cmdlet 來取得指定的記錄集，然後將它儲存在 $RecordSet 變數中。</span><span class="sxs-lookup"><span data-stu-id="da4cd-118">The first command uses the **Get-AzureRmDnsRecordset** cmdlet to get the specified record set, and then stores it in the $RecordSet variable.</span></span>

<span data-ttu-id="da4cd-119">第二個命令會更新 $RecordSet 中指定的 SOA 記錄。</span><span class="sxs-lookup"><span data-stu-id="da4cd-119">The second command updates the specified SOA record in $RecordSet.</span></span>

<span data-ttu-id="da4cd-120">Final 命令會使用 **AzureRmDnsRecordSet** Cmdlet 來傳播 $RecordSet 中的更新。</span><span class="sxs-lookup"><span data-stu-id="da4cd-120">The final command uses the **Set-AzureRmDnsRecordSet** cmdlet to propagate the update in $RecordSet.</span></span>

## <span data-ttu-id="da4cd-121">參數</span><span class="sxs-lookup"><span data-stu-id="da4cd-121">PARAMETERS</span></span>

### <span data-ttu-id="da4cd-122">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="da4cd-122">-Overwrite</span></span>
<span data-ttu-id="da4cd-123">指示更新記錄集（不論併發變更）。</span><span class="sxs-lookup"><span data-stu-id="da4cd-123">Indicates to update the record set regardless of concurrent changes.</span></span>

<span data-ttu-id="da4cd-124">如果自檢索到本機 **RecordSet** 物件之後，在 Azure DNS 中變更記錄集，則不會更新。</span><span class="sxs-lookup"><span data-stu-id="da4cd-124">The record set will not be updated if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="da4cd-125">這可為併發變更提供保護。</span><span class="sxs-lookup"><span data-stu-id="da4cd-125">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="da4cd-126">若要取消此行為，您可以使用 *Overwrite* 參數，不論併發變更為何，都會更新記錄集合。</span><span class="sxs-lookup"><span data-stu-id="da4cd-126">To suppress this behavior, you can use the *Overwrite* parameter, which results in the record set being updated regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="da4cd-127">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="da4cd-127">-RecordSet</span></span>
<span data-ttu-id="da4cd-128">指定要更新的 **記錄集** 。</span><span class="sxs-lookup"><span data-stu-id="da4cd-128">Specifies the **RecordSet** to update.</span></span>

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

### <span data-ttu-id="da4cd-129">-確認</span><span class="sxs-lookup"><span data-stu-id="da4cd-129">-Confirm</span></span>
<span data-ttu-id="da4cd-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="da4cd-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da4cd-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da4cd-131">-WhatIf</span></span>
<span data-ttu-id="da4cd-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="da4cd-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="da4cd-133">未執行 Cmdlet。顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="da4cd-133">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="da4cd-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="da4cd-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da4cd-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da4cd-135">-DefaultProfile</span></span>
<span data-ttu-id="da4cd-136">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="da4cd-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="da4cd-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da4cd-137">CommonParameters</span></span>
<span data-ttu-id="da4cd-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="da4cd-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da4cd-139">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="da4cd-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da4cd-140">輸入</span><span class="sxs-lookup"><span data-stu-id="da4cd-140">INPUTS</span></span>

### <span data-ttu-id="da4cd-141">DnsRecordSet （）</span><span class="sxs-lookup"><span data-stu-id="da4cd-141">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="da4cd-142">您可以將 **RecordSet** 物件傳遞到這個 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="da4cd-142">You can pass a **RecordSet** object to this cmdlet.</span></span>

## <span data-ttu-id="da4cd-143">輸出</span><span class="sxs-lookup"><span data-stu-id="da4cd-143">OUTPUTS</span></span>

### <span data-ttu-id="da4cd-144">DnsRecordSet （）</span><span class="sxs-lookup"><span data-stu-id="da4cd-144">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="da4cd-145">這個 Cmdlet 會傳回代表更新之 **RecordSet** 物件的物件。</span><span class="sxs-lookup"><span data-stu-id="da4cd-145">This cmdlet returns an object that represents the updated **RecordSet** object.</span></span>

## <span data-ttu-id="da4cd-146">筆記</span><span class="sxs-lookup"><span data-stu-id="da4cd-146">NOTES</span></span>
<span data-ttu-id="da4cd-147">您可以使用 *Confirm* 參數來控制此 Cmdlet 是否提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="da4cd-147">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="da4cd-148">根據預設，如果 $ConfirmPreference 的 Windows PowerShell 變數的值為 [中] 或 [低]，則該 Cmdlet 會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="da4cd-148">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>

<span data-ttu-id="da4cd-149">如果您指定 [ *確認* ] 或 [ *確認]： $True* ，此 Cmdlet 會在您執行之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="da4cd-149">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="da4cd-150">如果您指定 [ *確認： $False* ]，則 Cmdlet 不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="da4cd-150">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span> 

## <span data-ttu-id="da4cd-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="da4cd-151">RELATED LINKS</span></span>

[<span data-ttu-id="da4cd-152">AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="da4cd-152">Get-AzureRmDnsRecordSet</span></span>](./Get-AzureRmDnsRecordSet.md)

[<span data-ttu-id="da4cd-153">新-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="da4cd-153">New-AzureRmDnsRecordSet</span></span>](./New-AzureRmDnsRecordSet.md)

[<span data-ttu-id="da4cd-154">移除-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="da4cd-154">Remove-AzureRmDnsRecordSet</span></span>](./Remove-AzureRmDnsRecordSet.md)
