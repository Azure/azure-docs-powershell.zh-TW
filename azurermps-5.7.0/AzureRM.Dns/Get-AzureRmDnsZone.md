---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: B831ABE6-348C-4DD6-9295-18D23A1FDF63
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.dns/get-azurermdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Get-AzureRmDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Get-AzureRmDnsZone.md
ms.openlocfilehash: d25cca457adb70398d29b1b2a8044ac14af893db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624728"
---
# <span data-ttu-id="ce6d2-101">Get-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="ce6d2-101">Get-AzureRmDnsZone</span></span>

## <span data-ttu-id="ce6d2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ce6d2-102">SYNOPSIS</span></span>
<span data-ttu-id="ce6d2-103">取得 DNS 區域。</span><span class="sxs-lookup"><span data-stu-id="ce6d2-103">Gets a DNS zone.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ce6d2-104">句法</span><span class="sxs-lookup"><span data-stu-id="ce6d2-104">SYNTAX</span></span>

### <span data-ttu-id="ce6d2-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="ce6d2-105">Default (Default)</span></span>
```
Get-AzureRmDnsZone [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ce6d2-106">資源</span><span class="sxs-lookup"><span data-stu-id="ce6d2-106">ResourceGroup</span></span>
```
Get-AzureRmDnsZone [-Name <String>] -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ce6d2-107">說明</span><span class="sxs-lookup"><span data-stu-id="ce6d2-107">DESCRIPTION</span></span>
<span data-ttu-id="ce6d2-108">**AzureRmDnsZone** Cmdlet 會從指定的資源群組 (DNS) 區域中取得網功能變數名稱稱系統。</span><span class="sxs-lookup"><span data-stu-id="ce6d2-108">The **Get-AzureRmDnsZone** cmdlet gets a Domain Name System (DNS) zone from the specified resource group.</span></span>
<span data-ttu-id="ce6d2-109">如果您指定 *Name* 參數，則會傳回單一 **DnsZone** 物件。</span><span class="sxs-lookup"><span data-stu-id="ce6d2-109">If you specify the *Name* parameter, a single **DnsZone** object is returned.</span></span>
<span data-ttu-id="ce6d2-110">如果您沒有指定 *Name* 參數，則會傳回包含指定資源群組中所有區域的陣列。</span><span class="sxs-lookup"><span data-stu-id="ce6d2-110">If you do not specify the *Name* parameter, an array containing all of the zones in the specified resource group is returned.</span></span>
<span data-ttu-id="ce6d2-111">您可以使用 **DnsZone** 物件來更新區域，例如，您可以將 **記錄集** 物件新增到其中。</span><span class="sxs-lookup"><span data-stu-id="ce6d2-111">You can use the **DnsZone** object to update the zone, for example you can add **RecordSet** objects to it.</span></span>

## <span data-ttu-id="ce6d2-112">示例</span><span class="sxs-lookup"><span data-stu-id="ce6d2-112">EXAMPLES</span></span>

### <span data-ttu-id="ce6d2-113">範例1：取得區域</span><span class="sxs-lookup"><span data-stu-id="ce6d2-113">Example 1: Get a zone</span></span>
```
PS C:\> $Zone = Get-AzureRmDnsZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com"
```

<span data-ttu-id="ce6d2-114">這個範例會從指定的資源群組取得名為 myzone.com 的 DNS 區域，然後將它儲存在 $Zone 變數中。</span><span class="sxs-lookup"><span data-stu-id="ce6d2-114">This example gets the DNS zone named myzone.com from the specified resource group, and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="ce6d2-115">範例2：取得資源群組中的所有區域</span><span class="sxs-lookup"><span data-stu-id="ce6d2-115">Example 2: Get all of the zones in a resource group</span></span>
```
PS C:\> $Zones = Get-AzureRmDnsZone -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="ce6d2-116">這個範例會取得指定資源群組中的所有 DNS 區域，然後將它儲存在 $Zones 變數中。</span><span class="sxs-lookup"><span data-stu-id="ce6d2-116">This example gets all of the DNS zones in the specified resource group, and then stores it in the $Zones variable.</span></span>

### <span data-ttu-id="ce6d2-117">範例3：取得訂閱中的所有區域</span><span class="sxs-lookup"><span data-stu-id="ce6d2-117">Example 3: Get all of the zones in a subscription</span></span>
```
PS C:\> $Zones = Get-AzureRmDnsZone
```

<span data-ttu-id="ce6d2-118">這個範例會取得目前 Azure 訂閱中的所有 DNS 區域，然後將它們儲存在 $Zones 變數中。</span><span class="sxs-lookup"><span data-stu-id="ce6d2-118">This example gets all of the DNS zones in the current Azure subscription, and then stores them in the $Zones variable.</span></span>

## <span data-ttu-id="ce6d2-119">參數</span><span class="sxs-lookup"><span data-stu-id="ce6d2-119">PARAMETERS</span></span>

### <span data-ttu-id="ce6d2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce6d2-120">-DefaultProfile</span></span>
<span data-ttu-id="ce6d2-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="ce6d2-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce6d2-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="ce6d2-122">-Name</span></span>
<span data-ttu-id="ce6d2-123">指定要取得的 DNS 區功能變數名稱稱。</span><span class="sxs-lookup"><span data-stu-id="ce6d2-123">Specifies the name of the DNS zone to get.</span></span>

<span data-ttu-id="ce6d2-124">如果您沒有指定 *Name* 參數的值，這個 Cmdlet 會取得指定資源群組中的所有 DNS 區域。</span><span class="sxs-lookup"><span data-stu-id="ce6d2-124">If you do not specify a value for the *Name* parameter, this cmdlet gets all DNS zones in the specified resource group.</span></span>
<span data-ttu-id="ce6d2-125">如果您也省略 *ResourceGroupName* 參數，這個 Cmdlet 會取得目前 Azure 訂閱中的所有 DNS 區域。</span><span class="sxs-lookup"><span data-stu-id="ce6d2-125">If you also omit the *ResourceGroupName* parameter, this cmdlet gets all DNS zones in the current Azure subscription.</span></span>

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

### <span data-ttu-id="ce6d2-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce6d2-126">-ResourceGroupName</span></span>
<span data-ttu-id="ce6d2-127">指定包含要取得之 DNS 區域之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ce6d2-127">Specifies the name of the resource group that contains the DNS zone to get.</span></span>

<span data-ttu-id="ce6d2-128">如果您沒有指定 *ResourceGroupName* ，則您也必須省略 *Name* 參數。</span><span class="sxs-lookup"><span data-stu-id="ce6d2-128">If you do not specify the *ResourceGroupName* , then you must also omit the *Name* parameter.</span></span>
<span data-ttu-id="ce6d2-129">在這種情況下，這個 Cmdlet 會取得目前 Azure 訂閱中的所有 DNS 區域。</span><span class="sxs-lookup"><span data-stu-id="ce6d2-129">In this case, this cmdlet gets all DNS zones in the current Azure subscription.</span></span>

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

### <span data-ttu-id="ce6d2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce6d2-130">CommonParameters</span></span>
<span data-ttu-id="ce6d2-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ce6d2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce6d2-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ce6d2-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce6d2-133">輸入</span><span class="sxs-lookup"><span data-stu-id="ce6d2-133">INPUTS</span></span>

### <span data-ttu-id="ce6d2-134">所有</span><span class="sxs-lookup"><span data-stu-id="ce6d2-134">None</span></span>
<span data-ttu-id="ce6d2-135">這個 Cmdlet 不允許您進行管道輸入。</span><span class="sxs-lookup"><span data-stu-id="ce6d2-135">This cmdlet does not allow you to pipe input.</span></span>

## <span data-ttu-id="ce6d2-136">輸出</span><span class="sxs-lookup"><span data-stu-id="ce6d2-136">OUTPUTS</span></span>

### <span data-ttu-id="ce6d2-137">DnsZone （）</span><span class="sxs-lookup"><span data-stu-id="ce6d2-137">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="ce6d2-138">這個 Cmdlet 會傳回代表 DNS 區域的物件。</span><span class="sxs-lookup"><span data-stu-id="ce6d2-138">This cmdlet returns an object that represents the DNS zone.</span></span>
<span data-ttu-id="ce6d2-139">如果未指定區功能變數名稱稱，則會傳回區域物件的陣列。</span><span class="sxs-lookup"><span data-stu-id="ce6d2-139">If the zone name is not specified, an array of zone objects is returned.</span></span>

## <span data-ttu-id="ce6d2-140">筆記</span><span class="sxs-lookup"><span data-stu-id="ce6d2-140">NOTES</span></span>

## <span data-ttu-id="ce6d2-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="ce6d2-141">RELATED LINKS</span></span>

[<span data-ttu-id="ce6d2-142">新-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="ce6d2-142">New-AzureRmDnsZone</span></span>](./New-AzureRmDnsZone.md)

[<span data-ttu-id="ce6d2-143">移除-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="ce6d2-143">Remove-AzureRmDnsZone</span></span>](./Remove-AzureRmDnsZone.md)

[<span data-ttu-id="ce6d2-144">Set-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="ce6d2-144">Set-AzureRmDnsZone</span></span>](./Set-AzureRmDnsZone.md)
