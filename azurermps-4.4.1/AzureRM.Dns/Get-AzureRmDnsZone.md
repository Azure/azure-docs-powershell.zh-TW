---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: B831ABE6-348C-4DD6-9295-18D23A1FDF63
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Get-AzureRmDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Get-AzureRmDnsZone.md
ms.openlocfilehash: eabf0809aebf50458d15b195a5ec9afc4f0b9cf1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625511"
---
# <span data-ttu-id="e6fab-101">Get-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="e6fab-101">Get-AzureRmDnsZone</span></span>

## <span data-ttu-id="e6fab-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e6fab-102">SYNOPSIS</span></span>
<span data-ttu-id="e6fab-103">取得 DNS 區域。</span><span class="sxs-lookup"><span data-stu-id="e6fab-103">Gets a DNS zone.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e6fab-104">句法</span><span class="sxs-lookup"><span data-stu-id="e6fab-104">SYNTAX</span></span>

### <span data-ttu-id="e6fab-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="e6fab-105">Default (Default)</span></span>
```
Get-AzureRmDnsZone [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e6fab-106">資源</span><span class="sxs-lookup"><span data-stu-id="e6fab-106">ResourceGroup</span></span>
```
Get-AzureRmDnsZone [-Name <String>] -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e6fab-107">說明</span><span class="sxs-lookup"><span data-stu-id="e6fab-107">DESCRIPTION</span></span>
<span data-ttu-id="e6fab-108">**AzureRmDnsZone** Cmdlet 會從指定的資源群組 (DNS) 區域中取得網功能變數名稱稱系統。</span><span class="sxs-lookup"><span data-stu-id="e6fab-108">The **Get-AzureRmDnsZone** cmdlet gets a Domain Name System (DNS) zone from the specified resource group.</span></span>
<span data-ttu-id="e6fab-109">如果您指定 *Name* 參數，則會傳回單一 **DnsZone** 物件。</span><span class="sxs-lookup"><span data-stu-id="e6fab-109">If you specify the *Name* parameter, a single **DnsZone** object is returned.</span></span>
<span data-ttu-id="e6fab-110">如果您沒有指定 *Name* 參數，則會傳回包含指定資源群組中所有區域的陣列。</span><span class="sxs-lookup"><span data-stu-id="e6fab-110">If you do not specify the *Name* parameter, an array containing all of the zones in the specified resource group is returned.</span></span>
<span data-ttu-id="e6fab-111">您可以使用 **DnsZone** 物件來更新區域，例如，您可以將 **記錄集** 物件新增到其中。</span><span class="sxs-lookup"><span data-stu-id="e6fab-111">You can use the **DnsZone** object to update the zone, for example you can add **RecordSet** objects to it.</span></span>

## <span data-ttu-id="e6fab-112">示例</span><span class="sxs-lookup"><span data-stu-id="e6fab-112">EXAMPLES</span></span>

### <span data-ttu-id="e6fab-113">範例1：取得區域</span><span class="sxs-lookup"><span data-stu-id="e6fab-113">Example 1: Get a zone</span></span>
```
PS C:\> $Zone = Get-AzureRmDnsZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com"
```

<span data-ttu-id="e6fab-114">這個範例會從指定的資源群組取得名為 myzone.com 的 DNS 區域，然後將它儲存在 $Zone 變數中。</span><span class="sxs-lookup"><span data-stu-id="e6fab-114">This example gets the DNS zone named myzone.com from the specified resource group, and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="e6fab-115">範例2：取得資源群組中的所有區域</span><span class="sxs-lookup"><span data-stu-id="e6fab-115">Example 2: Get all of the zones in a resource group</span></span>
```
PS C:\> $Zones = Get-AzureRmDnsZone -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="e6fab-116">這個範例會取得指定資源群組中的所有 DNS 區域，然後將它儲存在 $Zones 變數中。</span><span class="sxs-lookup"><span data-stu-id="e6fab-116">This example gets all of the DNS zones in the specified resource group, and then stores it in the $Zones variable.</span></span>

### <span data-ttu-id="e6fab-117">範例3：取得訂閱中的所有區域</span><span class="sxs-lookup"><span data-stu-id="e6fab-117">Example 3: Get all of the zones in a subscription</span></span>
```
PS C:\> $Zones = Get-AzureRmDnsZone
```

<span data-ttu-id="e6fab-118">這個範例會取得目前 Azure 訂閱中的所有 DNS 區域，然後將它們儲存在 $Zones 變數中。</span><span class="sxs-lookup"><span data-stu-id="e6fab-118">This example gets all of the DNS zones in the current Azure subscription, and then stores them in the $Zones variable.</span></span>

## <span data-ttu-id="e6fab-119">參數</span><span class="sxs-lookup"><span data-stu-id="e6fab-119">PARAMETERS</span></span>

### <span data-ttu-id="e6fab-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="e6fab-120">-Name</span></span>
<span data-ttu-id="e6fab-121">指定要取得的 DNS 區功能變數名稱稱。</span><span class="sxs-lookup"><span data-stu-id="e6fab-121">Specifies the name of the DNS zone to get.</span></span>

<span data-ttu-id="e6fab-122">如果您沒有指定 *Name* 參數的值，這個 Cmdlet 會取得指定資源群組中的所有 DNS 區域。</span><span class="sxs-lookup"><span data-stu-id="e6fab-122">If you do not specify a value for the *Name* parameter, this cmdlet gets all DNS zones in the specified resource group.</span></span>
<span data-ttu-id="e6fab-123">如果您也省略 *ResourceGroupName* 參數，這個 Cmdlet 會取得目前 Azure 訂閱中的所有 DNS 區域。</span><span class="sxs-lookup"><span data-stu-id="e6fab-123">If you also omit the *ResourceGroupName* parameter, this cmdlet gets all DNS zones in the current Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroup
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6fab-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6fab-124">-ResourceGroupName</span></span>
<span data-ttu-id="e6fab-125">指定包含要取得之 DNS 區域之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e6fab-125">Specifies the name of the resource group that contains the DNS zone to get.</span></span>

<span data-ttu-id="e6fab-126">如果您沒有指定 *ResourceGroupName* ，則您也必須省略 *Name* 參數。</span><span class="sxs-lookup"><span data-stu-id="e6fab-126">If you do not specify the *ResourceGroupName* , then you must also omit the *Name* parameter.</span></span>
<span data-ttu-id="e6fab-127">在這種情況下，這個 Cmdlet 會取得目前 Azure 訂閱中的所有 DNS 區域。</span><span class="sxs-lookup"><span data-stu-id="e6fab-127">In this case, this cmdlet gets all DNS zones in the current Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6fab-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6fab-128">-DefaultProfile</span></span>
<span data-ttu-id="e6fab-129">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e6fab-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e6fab-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6fab-130">CommonParameters</span></span>
<span data-ttu-id="e6fab-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e6fab-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6fab-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e6fab-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6fab-133">輸入</span><span class="sxs-lookup"><span data-stu-id="e6fab-133">INPUTS</span></span>

### <span data-ttu-id="e6fab-134">所有</span><span class="sxs-lookup"><span data-stu-id="e6fab-134">None</span></span>
<span data-ttu-id="e6fab-135">這個 Cmdlet 不允許您進行管道輸入。</span><span class="sxs-lookup"><span data-stu-id="e6fab-135">This cmdlet does not allow you to pipe input.</span></span>

## <span data-ttu-id="e6fab-136">輸出</span><span class="sxs-lookup"><span data-stu-id="e6fab-136">OUTPUTS</span></span>

### <span data-ttu-id="e6fab-137">DnsZone （）</span><span class="sxs-lookup"><span data-stu-id="e6fab-137">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="e6fab-138">這個 Cmdlet 會傳回代表 DNS 區域的物件。</span><span class="sxs-lookup"><span data-stu-id="e6fab-138">This cmdlet returns an object that represents the DNS zone.</span></span>
<span data-ttu-id="e6fab-139">如果未指定區功能變數名稱稱，則會傳回區域物件的陣列。</span><span class="sxs-lookup"><span data-stu-id="e6fab-139">If the zone name is not specified, an array of zone objects is returned.</span></span>

## <span data-ttu-id="e6fab-140">筆記</span><span class="sxs-lookup"><span data-stu-id="e6fab-140">NOTES</span></span>

## <span data-ttu-id="e6fab-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="e6fab-141">RELATED LINKS</span></span>

[<span data-ttu-id="e6fab-142">新-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="e6fab-142">New-AzureRmDnsZone</span></span>](./New-AzureRmDnsZone.md)

[<span data-ttu-id="e6fab-143">移除-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="e6fab-143">Remove-AzureRmDnsZone</span></span>](./Remove-AzureRmDnsZone.md)

[<span data-ttu-id="e6fab-144">Set-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="e6fab-144">Set-AzureRmDnsZone</span></span>](./Set-AzureRmDnsZone.md)
