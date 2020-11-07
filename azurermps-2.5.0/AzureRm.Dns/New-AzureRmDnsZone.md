---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
ms.assetid: B78F3E8B-C7D2-458C-AB23-06F584FE97E0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 46b14399d1cae624f4735111d809702cfd14180e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801009"
---
# <span data-ttu-id="ea5c8-101">New-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="ea5c8-101">New-AzureRmDnsZone</span></span>

## <span data-ttu-id="ea5c8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ea5c8-102">SYNOPSIS</span></span>
<span data-ttu-id="ea5c8-103">建立新的 DNS 區域。</span><span class="sxs-lookup"><span data-stu-id="ea5c8-103">Creates a new DNS zone.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ea5c8-104">句法</span><span class="sxs-lookup"><span data-stu-id="ea5c8-104">SYNTAX</span></span>

```
New-AzureRmDnsZone -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ea5c8-105">說明</span><span class="sxs-lookup"><span data-stu-id="ea5c8-105">DESCRIPTION</span></span>
<span data-ttu-id="ea5c8-106">**新的-AzureRmDnsZone** Cmdlet 會在指定的資源群組 (DNS) 區域中建立新的網域名稱系統。</span><span class="sxs-lookup"><span data-stu-id="ea5c8-106">The **New-AzureRmDnsZone** cmdlet creates a new Domain Name System (DNS) zone in the specified resource group.</span></span> <span data-ttu-id="ea5c8-107">您必須為 *name* 參數指定唯一的 DNS 區功能變數名稱稱，否則 Cmdlet 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="ea5c8-107">You must specify a unique DNS zone name for the *Name* parameter or the cmdlet will return an error.</span></span> <span data-ttu-id="ea5c8-108">建立區域之後，請使用 New-AzureRmDnsRecordSet Cmdlet 來建立區域中的記錄集。</span><span class="sxs-lookup"><span data-stu-id="ea5c8-108">After the zone is created, use the New-AzureRmDnsRecordSet cmdlet to create record sets in the zone.</span></span>

<span data-ttu-id="ea5c8-109">您可以使用 *Confirm* 參數和 $ConfirmPreference 的 Windows PowerShell 變數來控制 Cmdlet 是否提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ea5c8-109">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="ea5c8-110">示例</span><span class="sxs-lookup"><span data-stu-id="ea5c8-110">EXAMPLES</span></span>

### <span data-ttu-id="ea5c8-111">範例1：建立 DNS 區域</span><span class="sxs-lookup"><span data-stu-id="ea5c8-111">Example 1: Create a DNS zone</span></span>
```
PS C:\>$Zone = New-AzureRmDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="ea5c8-112">這個命令會在指定的資源群組中建立名為 myzone.com 的新 DNS 區域，然後將它儲存在 $Zone 變數中。</span><span class="sxs-lookup"><span data-stu-id="ea5c8-112">This command creates a new DNS zone named myzone.com in the specified resource group, and then stores it in the $Zone variable.</span></span>

## <span data-ttu-id="ea5c8-113">參數</span><span class="sxs-lookup"><span data-stu-id="ea5c8-113">PARAMETERS</span></span>

### <span data-ttu-id="ea5c8-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="ea5c8-114">-Name</span></span>
<span data-ttu-id="ea5c8-115">指定要建立之 DNS 區域的名稱。</span><span class="sxs-lookup"><span data-stu-id="ea5c8-115">Specifies the name of the DNS zone to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea5c8-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea5c8-116">-ResourceGroupName</span></span>
<span data-ttu-id="ea5c8-117">指定要在其中建立區域的資源群組。</span><span class="sxs-lookup"><span data-stu-id="ea5c8-117">Specifies the resource group in which to create the zone.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea5c8-118">-Tag</span><span class="sxs-lookup"><span data-stu-id="ea5c8-118">-Tag</span></span>
<span data-ttu-id="ea5c8-119">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="ea5c8-119">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="ea5c8-120">例如：</span><span class="sxs-lookup"><span data-stu-id="ea5c8-120">For example:</span></span>

<span data-ttu-id="ea5c8-121">@ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="ea5c8-121">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea5c8-122">-確認</span><span class="sxs-lookup"><span data-stu-id="ea5c8-122">-Confirm</span></span>
<span data-ttu-id="ea5c8-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ea5c8-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea5c8-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea5c8-124">-WhatIf</span></span>
<span data-ttu-id="ea5c8-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ea5c8-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ea5c8-126">未執行 Cmdlet。顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ea5c8-126">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ea5c8-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ea5c8-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea5c8-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea5c8-128">CommonParameters</span></span>
<span data-ttu-id="ea5c8-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ea5c8-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea5c8-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ea5c8-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea5c8-131">輸入</span><span class="sxs-lookup"><span data-stu-id="ea5c8-131">INPUTS</span></span>

### <span data-ttu-id="ea5c8-132">所有</span><span class="sxs-lookup"><span data-stu-id="ea5c8-132">None</span></span>

<span data-ttu-id="ea5c8-133">您無法將輸入管到這個 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ea5c8-133">You cannot pipe input to this cmdlet.</span></span>

## <span data-ttu-id="ea5c8-134">輸出</span><span class="sxs-lookup"><span data-stu-id="ea5c8-134">OUTPUTS</span></span>

### <span data-ttu-id="ea5c8-135">DnsZone （）</span><span class="sxs-lookup"><span data-stu-id="ea5c8-135">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

<span data-ttu-id="ea5c8-136">這個 Cmdlet 會傳回代表新的 DNS 區域的 DnsZone 物件。</span><span class="sxs-lookup"><span data-stu-id="ea5c8-136">This cmdlet returns a Microsoft.Azure.Commands.Dns.DnsZone object that represents the new DNS zone.</span></span>

## <span data-ttu-id="ea5c8-137">筆記</span><span class="sxs-lookup"><span data-stu-id="ea5c8-137">NOTES</span></span>
<span data-ttu-id="ea5c8-138">您可以使用 *Confirm* 參數來控制此 Cmdlet 是否提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ea5c8-138">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="ea5c8-139">根據預設，如果 $ConfirmPreference 的 Windows PowerShell 變數的值為 [中] 或 [低]，則該 Cmdlet 會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ea5c8-139">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>

<span data-ttu-id="ea5c8-140">如果您指定 [ *確認* ] 或 [ *確認]： $True* ，此 Cmdlet 會在您執行之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ea5c8-140">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="ea5c8-141">如果您指定 [ *確認： $False* ]，則 Cmdlet 不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ea5c8-141">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="ea5c8-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="ea5c8-142">RELATED LINKS</span></span>

[<span data-ttu-id="ea5c8-143">AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="ea5c8-143">Get-AzureRmDnsZone</span></span>](./Get-AzureRmDnsZone.md)

[<span data-ttu-id="ea5c8-144">新-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="ea5c8-144">New-AzureRmDnsRecordSet</span></span>](./New-AzureRmDnsRecordSet.md)

[<span data-ttu-id="ea5c8-145">移除-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="ea5c8-145">Remove-AzureRmDnsZone</span></span>](./Remove-AzureRmDnsZone.md)
