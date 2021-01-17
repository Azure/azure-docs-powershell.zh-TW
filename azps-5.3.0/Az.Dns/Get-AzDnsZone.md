---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: B831ABE6-348C-4DD6-9295-18D23A1FDF63
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/get-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsZone.md
ms.openlocfilehash: 68fff050564eff7014a7428556d3d4b2ce68f06d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98435179"
---
# <span data-ttu-id="35d57-101">Get-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="35d57-101">Get-AzDnsZone</span></span>

## <span data-ttu-id="35d57-102">摘要</span><span class="sxs-lookup"><span data-stu-id="35d57-102">SYNOPSIS</span></span>
<span data-ttu-id="35d57-103">取得 DNS 區域。</span><span class="sxs-lookup"><span data-stu-id="35d57-103">Gets a DNS zone.</span></span>

## <span data-ttu-id="35d57-104">句法</span><span class="sxs-lookup"><span data-stu-id="35d57-104">SYNTAX</span></span>

### <span data-ttu-id="35d57-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="35d57-105">Default (Default)</span></span>
```
Get-AzDnsZone [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="35d57-106">資源</span><span class="sxs-lookup"><span data-stu-id="35d57-106">ResourceGroup</span></span>
```
Get-AzDnsZone [-Name <String>] -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="35d57-107">說明</span><span class="sxs-lookup"><span data-stu-id="35d57-107">DESCRIPTION</span></span>
<span data-ttu-id="35d57-108">**AzDnsZone** Cmdlet 會從指定的資源群組 (DNS) 區域中取得網功能變數名稱稱系統。</span><span class="sxs-lookup"><span data-stu-id="35d57-108">The **Get-AzDnsZone** cmdlet gets a Domain Name System (DNS) zone from the specified resource group.</span></span>
<span data-ttu-id="35d57-109">如果您指定 *Name* 參數，則會傳回單一 **DnsZone** 物件。</span><span class="sxs-lookup"><span data-stu-id="35d57-109">If you specify the *Name* parameter, a single **DnsZone** object is returned.</span></span>
<span data-ttu-id="35d57-110">如果您沒有指定 *Name* 參數，則會傳回包含指定資源群組中所有區域的陣列。</span><span class="sxs-lookup"><span data-stu-id="35d57-110">If you do not specify the *Name* parameter, an array containing all of the zones in the specified resource group is returned.</span></span>
<span data-ttu-id="35d57-111">您可以使用 **DnsZone** 物件來更新區域，例如，您可以將 **記錄集** 物件新增到其中。</span><span class="sxs-lookup"><span data-stu-id="35d57-111">You can use the **DnsZone** object to update the zone, for example you can add **RecordSet** objects to it.</span></span>

## <span data-ttu-id="35d57-112">示例</span><span class="sxs-lookup"><span data-stu-id="35d57-112">EXAMPLES</span></span>

### <span data-ttu-id="35d57-113">範例1：取得區域</span><span class="sxs-lookup"><span data-stu-id="35d57-113">Example 1: Get a zone</span></span>
```
PS C:\> $Zone = Get-AzDnsZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com"
```

<span data-ttu-id="35d57-114">這個範例會從指定的資源群組取得名為 myzone.com 的 DNS 區域，然後將它儲存在 $Zone 變數中。</span><span class="sxs-lookup"><span data-stu-id="35d57-114">This example gets the DNS zone named myzone.com from the specified resource group, and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="35d57-115">範例2：取得資源群組中的所有區域</span><span class="sxs-lookup"><span data-stu-id="35d57-115">Example 2: Get all of the zones in a resource group</span></span>
```
PS C:\> $Zones = Get-AzDnsZone -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="35d57-116">這個範例會取得指定資源群組中的所有 DNS 區域，然後將它儲存在 $Zones 變數中。</span><span class="sxs-lookup"><span data-stu-id="35d57-116">This example gets all of the DNS zones in the specified resource group, and then stores it in the $Zones variable.</span></span>

### <span data-ttu-id="35d57-117">範例3：取得訂閱中的所有區域</span><span class="sxs-lookup"><span data-stu-id="35d57-117">Example 3: Get all of the zones in a subscription</span></span>
```
PS C:\> $Zones = Get-AzDnsZone
```

<span data-ttu-id="35d57-118">這個範例會取得目前 Azure 訂閱中的所有 DNS 區域，然後將它們儲存在 $Zones 變數中。</span><span class="sxs-lookup"><span data-stu-id="35d57-118">This example gets all of the DNS zones in the current Azure subscription, and then stores them in the $Zones variable.</span></span>

## <span data-ttu-id="35d57-119">參數</span><span class="sxs-lookup"><span data-stu-id="35d57-119">PARAMETERS</span></span>

### <span data-ttu-id="35d57-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35d57-120">-DefaultProfile</span></span>
<span data-ttu-id="35d57-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="35d57-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="35d57-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="35d57-122">-Name</span></span>
<span data-ttu-id="35d57-123">指定要取得的 DNS 區功能變數名稱稱。</span><span class="sxs-lookup"><span data-stu-id="35d57-123">Specifies the name of the DNS zone to get.</span></span>
<span data-ttu-id="35d57-124">如果您沒有指定 *Name* 參數的值，這個 Cmdlet 會取得指定資源群組中的所有 DNS 區域。</span><span class="sxs-lookup"><span data-stu-id="35d57-124">If you do not specify a value for the *Name* parameter, this cmdlet gets all DNS zones in the specified resource group.</span></span>
<span data-ttu-id="35d57-125">如果您也省略 *ResourceGroupName* 參數，這個 Cmdlet 會取得目前 Azure 訂閱中的所有 DNS 區域。</span><span class="sxs-lookup"><span data-stu-id="35d57-125">If you also omit the *ResourceGroupName* parameter, this cmdlet gets all DNS zones in the current Azure subscription.</span></span>

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

### <span data-ttu-id="35d57-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35d57-126">-ResourceGroupName</span></span>
<span data-ttu-id="35d57-127">指定包含要取得之 DNS 區域之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="35d57-127">Specifies the name of the resource group that contains the DNS zone to get.</span></span>
<span data-ttu-id="35d57-128">如果您沒有指定 *ResourceGroupName*，則您也必須省略 *Name* 參數。</span><span class="sxs-lookup"><span data-stu-id="35d57-128">If you do not specify the *ResourceGroupName*, then you must also omit the *Name* parameter.</span></span>
<span data-ttu-id="35d57-129">在這種情況下，這個 Cmdlet 會取得目前 Azure 訂閱中的所有 DNS 區域。</span><span class="sxs-lookup"><span data-stu-id="35d57-129">In this case, this cmdlet gets all DNS zones in the current Azure subscription.</span></span>

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

### <span data-ttu-id="35d57-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35d57-130">CommonParameters</span></span>
<span data-ttu-id="35d57-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="35d57-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35d57-132">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="35d57-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35d57-133">輸入</span><span class="sxs-lookup"><span data-stu-id="35d57-133">INPUTS</span></span>

### <span data-ttu-id="35d57-134">System.object</span><span class="sxs-lookup"><span data-stu-id="35d57-134">System.String</span></span>

## <span data-ttu-id="35d57-135">輸出</span><span class="sxs-lookup"><span data-stu-id="35d57-135">OUTPUTS</span></span>

### <span data-ttu-id="35d57-136">DnsZone （）</span><span class="sxs-lookup"><span data-stu-id="35d57-136">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

## <span data-ttu-id="35d57-137">筆記</span><span class="sxs-lookup"><span data-stu-id="35d57-137">NOTES</span></span>

## <span data-ttu-id="35d57-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="35d57-138">RELATED LINKS</span></span>

[<span data-ttu-id="35d57-139">新-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="35d57-139">New-AzDnsZone</span></span>](./New-AzDnsZone.md)

[<span data-ttu-id="35d57-140">移除-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="35d57-140">Remove-AzDnsZone</span></span>](./Remove-AzDnsZone.md)

[<span data-ttu-id="35d57-141">Set-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="35d57-141">Set-AzDnsZone</span></span>](./Set-AzDnsZone.md)
