---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: B831ABE6-348C-4DD6-9295-18D23A1FDF63
online version: https://docs.microsoft.com/powershell/module/az.dns/get-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsZone.md
ms.openlocfilehash: a788cf3638d124dac164f19171f1be89afc2e385
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910145"
---
# <span data-ttu-id="b56ac-101">Get-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="b56ac-101">Get-AzDnsZone</span></span>

## <span data-ttu-id="b56ac-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b56ac-102">SYNOPSIS</span></span>
<span data-ttu-id="b56ac-103">獲得 DNS 區域。</span><span class="sxs-lookup"><span data-stu-id="b56ac-103">Gets a DNS zone.</span></span>

## <span data-ttu-id="b56ac-104">語法</span><span class="sxs-lookup"><span data-stu-id="b56ac-104">SYNTAX</span></span>

### <span data-ttu-id="b56ac-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="b56ac-105">Default (Default)</span></span>
```
Get-AzDnsZone [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b56ac-106">ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b56ac-106">ResourceGroup</span></span>
```
Get-AzDnsZone [-Name <String>] -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b56ac-107">描述</span><span class="sxs-lookup"><span data-stu-id="b56ac-107">DESCRIPTION</span></span>
<span data-ttu-id="b56ac-108">**Get-AzDnsZone** Cmdlet 會從指定的資源群組 (DNS) 區域取得網域名稱系統。</span><span class="sxs-lookup"><span data-stu-id="b56ac-108">The **Get-AzDnsZone** cmdlet gets a Domain Name System (DNS) zone from the specified resource group.</span></span>
<span data-ttu-id="b56ac-109">如果您指定 *Name* 參數，會返回單 **一 DnsZone** 物件。</span><span class="sxs-lookup"><span data-stu-id="b56ac-109">If you specify the *Name* parameter, a single **DnsZone** object is returned.</span></span>
<span data-ttu-id="b56ac-110">如果您未指定 *Name* 參數，則包含指定資源群組中所有區域之陣列會返回。</span><span class="sxs-lookup"><span data-stu-id="b56ac-110">If you do not specify the *Name* parameter, an array containing all of the zones in the specified resource group is returned.</span></span>
<span data-ttu-id="b56ac-111">您可以使用 **DnsZone 物件** 來更新區域，例如，您可以新增 **RecordSet** 物件至該區域。</span><span class="sxs-lookup"><span data-stu-id="b56ac-111">You can use the **DnsZone** object to update the zone, for example you can add **RecordSet** objects to it.</span></span>

## <span data-ttu-id="b56ac-112">例子</span><span class="sxs-lookup"><span data-stu-id="b56ac-112">EXAMPLES</span></span>

### <span data-ttu-id="b56ac-113">範例 1：取得區域</span><span class="sxs-lookup"><span data-stu-id="b56ac-113">Example 1: Get a zone</span></span>
```
PS C:\> $Zone = Get-AzDnsZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com"
```

<span data-ttu-id="b56ac-114">此範例會從指定的資源群組myzone.com DNS 區功能變數名稱稱，然後將它儲存在 $Zone 變數中。</span><span class="sxs-lookup"><span data-stu-id="b56ac-114">This example gets the DNS zone named myzone.com from the specified resource group, and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="b56ac-115">範例 2：取得資源群組的所有區域</span><span class="sxs-lookup"><span data-stu-id="b56ac-115">Example 2: Get all of the zones in a resource group</span></span>
```
PS C:\> $Zones = Get-AzDnsZone -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="b56ac-116">此範例會獲得指定資源群組中所有的 DNS 區域，然後將它儲存在$Zones變數。</span><span class="sxs-lookup"><span data-stu-id="b56ac-116">This example gets all of the DNS zones in the specified resource group, and then stores it in the $Zones variable.</span></span>

### <span data-ttu-id="b56ac-117">範例 3：取得訂閱的所有區域</span><span class="sxs-lookup"><span data-stu-id="b56ac-117">Example 3: Get all of the zones in a subscription</span></span>
```
PS C:\> $Zones = Get-AzDnsZone
```

<span data-ttu-id="b56ac-118">此範例會獲得目前 Azure 訂閱中所有的 DNS 區域，然後將它們儲存在 $Zones 變數中。</span><span class="sxs-lookup"><span data-stu-id="b56ac-118">This example gets all of the DNS zones in the current Azure subscription, and then stores them in the $Zones variable.</span></span>

## <span data-ttu-id="b56ac-119">參數</span><span class="sxs-lookup"><span data-stu-id="b56ac-119">PARAMETERS</span></span>

### <span data-ttu-id="b56ac-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b56ac-120">-DefaultProfile</span></span>
<span data-ttu-id="b56ac-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="b56ac-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b56ac-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="b56ac-122">-Name</span></span>
<span data-ttu-id="b56ac-123">指定要取得之 DNS 區域的名稱。</span><span class="sxs-lookup"><span data-stu-id="b56ac-123">Specifies the name of the DNS zone to get.</span></span>
<span data-ttu-id="b56ac-124">如果您沒有為 Name 參數指定值，此 Cmdlet 會獲得指定資源群組中所有的 DNS 區域。</span><span class="sxs-lookup"><span data-stu-id="b56ac-124">If you do not specify a value for the *Name* parameter, this cmdlet gets all DNS zones in the specified resource group.</span></span>
<span data-ttu-id="b56ac-125">如果您也省略 *ResourceGroupName* 參數，此 Cmdlet 會獲得目前 Azure 訂閱中所有的 DNS 區域。</span><span class="sxs-lookup"><span data-stu-id="b56ac-125">If you also omit the *ResourceGroupName* parameter, this cmdlet gets all DNS zones in the current Azure subscription.</span></span>

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

### <span data-ttu-id="b56ac-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b56ac-126">-ResourceGroupName</span></span>
<span data-ttu-id="b56ac-127">指定包含要取得 DNS 區域的資源組名。</span><span class="sxs-lookup"><span data-stu-id="b56ac-127">Specifies the name of the resource group that contains the DNS zone to get.</span></span>
<span data-ttu-id="b56ac-128">如果您未指定 *ResourceGroupName，* 則也必須省略 *Name* 參數。</span><span class="sxs-lookup"><span data-stu-id="b56ac-128">If you do not specify the *ResourceGroupName*, then you must also omit the *Name* parameter.</span></span>
<span data-ttu-id="b56ac-129">在此案例中，此 Cmdlet 會獲得目前 Azure 訂閱中所有的 DNS 區域。</span><span class="sxs-lookup"><span data-stu-id="b56ac-129">In this case, this cmdlet gets all DNS zones in the current Azure subscription.</span></span>

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

### <span data-ttu-id="b56ac-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b56ac-130">CommonParameters</span></span>
<span data-ttu-id="b56ac-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b56ac-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b56ac-132">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="b56ac-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b56ac-133">輸入</span><span class="sxs-lookup"><span data-stu-id="b56ac-133">INPUTS</span></span>

### <span data-ttu-id="b56ac-134">System.String</span><span class="sxs-lookup"><span data-stu-id="b56ac-134">System.String</span></span>

## <span data-ttu-id="b56ac-135">輸出</span><span class="sxs-lookup"><span data-stu-id="b56ac-135">OUTPUTS</span></span>

### <span data-ttu-id="b56ac-136">Microsoft.Azure.Commands.dns.DnsZone</span><span class="sxs-lookup"><span data-stu-id="b56ac-136">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

## <span data-ttu-id="b56ac-137">筆記</span><span class="sxs-lookup"><span data-stu-id="b56ac-137">NOTES</span></span>

## <span data-ttu-id="b56ac-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="b56ac-138">RELATED LINKS</span></span>

[<span data-ttu-id="b56ac-139">New-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="b56ac-139">New-AzDnsZone</span></span>](./New-AzDnsZone.md)

[<span data-ttu-id="b56ac-140">Remove-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="b56ac-140">Remove-AzDnsZone</span></span>](./Remove-AzDnsZone.md)

[<span data-ttu-id="b56ac-141">Set-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="b56ac-141">Set-AzDnsZone</span></span>](./Set-AzDnsZone.md)
