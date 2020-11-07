---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: B831ABE6-348C-4DD6-9295-18D23A1FDF63
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/get-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Get-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Get-AzDnsZone.md
ms.openlocfilehash: fe650e87635d16d3768bd527bf7422fe644c885e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795670"
---
# <span data-ttu-id="d0146-101">Get-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="d0146-101">Get-AzDnsZone</span></span>

## <span data-ttu-id="d0146-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d0146-102">SYNOPSIS</span></span>
<span data-ttu-id="d0146-103">取得 DNS 區域。</span><span class="sxs-lookup"><span data-stu-id="d0146-103">Gets a DNS zone.</span></span>

## <span data-ttu-id="d0146-104">句法</span><span class="sxs-lookup"><span data-stu-id="d0146-104">SYNTAX</span></span>

### <span data-ttu-id="d0146-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="d0146-105">Default (Default)</span></span>
```
Get-AzDnsZone [<CommonParameters>]
```

### <span data-ttu-id="d0146-106">資源</span><span class="sxs-lookup"><span data-stu-id="d0146-106">ResourceGroup</span></span>
```
Get-AzDnsZone [-Name <String>] -ResourceGroupName <String> [<CommonParameters>]
```

## <span data-ttu-id="d0146-107">說明</span><span class="sxs-lookup"><span data-stu-id="d0146-107">DESCRIPTION</span></span>
<span data-ttu-id="d0146-108">**AzDnsZone** Cmdlet 會從指定的資源群組 (DNS) 區域中取得網功能變數名稱稱系統。</span><span class="sxs-lookup"><span data-stu-id="d0146-108">The **Get-AzDnsZone** cmdlet gets a Domain Name System (DNS) zone from the specified resource group.</span></span>
<span data-ttu-id="d0146-109">如果您指定 *Name* 參數，則會傳回單一 **DnsZone** 物件。</span><span class="sxs-lookup"><span data-stu-id="d0146-109">If you specify the *Name* parameter, a single **DnsZone** object is returned.</span></span>
<span data-ttu-id="d0146-110">如果您沒有指定 *Name* 參數，則會傳回包含指定資源群組中所有區域的陣列。</span><span class="sxs-lookup"><span data-stu-id="d0146-110">If you do not specify the *Name* parameter, an array containing all of the zones in the specified resource group is returned.</span></span>
<span data-ttu-id="d0146-111">您可以使用 **DnsZone** 物件來更新區域，例如，您可以將 **記錄集** 物件新增到其中。</span><span class="sxs-lookup"><span data-stu-id="d0146-111">You can use the **DnsZone** object to update the zone, for example you can add **RecordSet** objects to it.</span></span>

## <span data-ttu-id="d0146-112">示例</span><span class="sxs-lookup"><span data-stu-id="d0146-112">EXAMPLES</span></span>

### <span data-ttu-id="d0146-113">範例1：取得區域</span><span class="sxs-lookup"><span data-stu-id="d0146-113">Example 1: Get a zone</span></span>
```
PS C:\> $Zone = Get-AzDnsZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com"
```

<span data-ttu-id="d0146-114">這個範例會從指定的資源群組取得名為 myzone.com 的 DNS 區域，然後將它儲存在 $Zone 變數中。</span><span class="sxs-lookup"><span data-stu-id="d0146-114">This example gets the DNS zone named myzone.com from the specified resource group, and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="d0146-115">範例2：取得資源群組中的所有區域</span><span class="sxs-lookup"><span data-stu-id="d0146-115">Example 2: Get all of the zones in a resource group</span></span>
```
PS C:\> $Zones = Get-AzDnsZone -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="d0146-116">這個範例會取得指定資源群組中的所有 DNS 區域，然後將它儲存在 $Zones 變數中。</span><span class="sxs-lookup"><span data-stu-id="d0146-116">This example gets all of the DNS zones in the specified resource group, and then stores it in the $Zones variable.</span></span>

### <span data-ttu-id="d0146-117">範例3：取得訂閱中的所有區域</span><span class="sxs-lookup"><span data-stu-id="d0146-117">Example 3: Get all of the zones in a subscription</span></span>
```
PS C:\> $Zones = Get-AzDnsZone
```

<span data-ttu-id="d0146-118">這個範例會取得目前 Azure 訂閱中的所有 DNS 區域，然後將它們儲存在 $Zones 變數中。</span><span class="sxs-lookup"><span data-stu-id="d0146-118">This example gets all of the DNS zones in the current Azure subscription, and then stores them in the $Zones variable.</span></span>

## <span data-ttu-id="d0146-119">參數</span><span class="sxs-lookup"><span data-stu-id="d0146-119">PARAMETERS</span></span>

### <span data-ttu-id="d0146-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="d0146-120">-Name</span></span>
<span data-ttu-id="d0146-121">指定要取得的 DNS 區功能變數名稱稱。</span><span class="sxs-lookup"><span data-stu-id="d0146-121">Specifies the name of the DNS zone to get.</span></span>

<span data-ttu-id="d0146-122">如果您沒有指定 *Name* 參數的值，這個 Cmdlet 會取得指定資源群組中的所有 DNS 區域。</span><span class="sxs-lookup"><span data-stu-id="d0146-122">If you do not specify a value for the *Name* parameter, this cmdlet gets all DNS zones in the specified resource group.</span></span>
<span data-ttu-id="d0146-123">如果您也省略 *ResourceGroupName* 參數，這個 Cmdlet 會取得目前 Azure 訂閱中的所有 DNS 區域。</span><span class="sxs-lookup"><span data-stu-id="d0146-123">If you also omit the *ResourceGroupName* parameter, this cmdlet gets all DNS zones in the current Azure subscription.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroup
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0146-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0146-124">-ResourceGroupName</span></span>
<span data-ttu-id="d0146-125">指定包含要取得之 DNS 區域之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d0146-125">Specifies the name of the resource group that contains the DNS zone to get.</span></span>

<span data-ttu-id="d0146-126">如果您沒有指定 *ResourceGroupName* ，則您也必須省略 *Name* 參數。</span><span class="sxs-lookup"><span data-stu-id="d0146-126">If you do not specify the *ResourceGroupName* , then you must also omit the *Name* parameter.</span></span>
<span data-ttu-id="d0146-127">在這種情況下，這個 Cmdlet 會取得目前 Azure 訂閱中的所有 DNS 區域。</span><span class="sxs-lookup"><span data-stu-id="d0146-127">In this case, this cmdlet gets all DNS zones in the current Azure subscription.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0146-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0146-128">CommonParameters</span></span>
<span data-ttu-id="d0146-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d0146-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0146-130">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d0146-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0146-131">輸入</span><span class="sxs-lookup"><span data-stu-id="d0146-131">INPUTS</span></span>

### <span data-ttu-id="d0146-132">所有</span><span class="sxs-lookup"><span data-stu-id="d0146-132">None</span></span>
<span data-ttu-id="d0146-133">這個 Cmdlet 不允許您進行管道輸入。</span><span class="sxs-lookup"><span data-stu-id="d0146-133">This cmdlet does not allow you to pipe input.</span></span>

## <span data-ttu-id="d0146-134">輸出</span><span class="sxs-lookup"><span data-stu-id="d0146-134">OUTPUTS</span></span>

### <span data-ttu-id="d0146-135">DnsZone （）</span><span class="sxs-lookup"><span data-stu-id="d0146-135">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="d0146-136">這個 Cmdlet 會傳回代表 DNS 區域的物件。</span><span class="sxs-lookup"><span data-stu-id="d0146-136">This cmdlet returns an object that represents the DNS zone.</span></span>
<span data-ttu-id="d0146-137">如果未指定區功能變數名稱稱，則會傳回區域物件的陣列。</span><span class="sxs-lookup"><span data-stu-id="d0146-137">If the zone name is not specified, an array of zone objects is returned.</span></span>

## <span data-ttu-id="d0146-138">筆記</span><span class="sxs-lookup"><span data-stu-id="d0146-138">NOTES</span></span>

## <span data-ttu-id="d0146-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="d0146-139">RELATED LINKS</span></span>

[<span data-ttu-id="d0146-140">新-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="d0146-140">New-AzDnsZone</span></span>](./New-AzDnsZone.md)

[<span data-ttu-id="d0146-141">移除-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="d0146-141">Remove-AzDnsZone</span></span>](./Remove-AzDnsZone.md)

[<span data-ttu-id="d0146-142">Set-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="d0146-142">Set-AzDnsZone</span></span>](./Set-AzDnsZone.md)
