---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/powershell/module/az.privatedns/get-azprivatednszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Get-AzPrivateDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Get-AzPrivateDnsZone.md
ms.openlocfilehash: 6cc89d9e5fad05bc26c824221831fcebcf833b21
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913342"
---
# <span data-ttu-id="edad8-101">Get-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="edad8-101">Get-AzPrivateDnsZone</span></span>

## <span data-ttu-id="edad8-102">簡介</span><span class="sxs-lookup"><span data-stu-id="edad8-102">SYNOPSIS</span></span>
<span data-ttu-id="edad8-103">獲得私人 DNS 區域。</span><span class="sxs-lookup"><span data-stu-id="edad8-103">Gets a Private DNS zone.</span></span>

## <span data-ttu-id="edad8-104">語法</span><span class="sxs-lookup"><span data-stu-id="edad8-104">SYNTAX</span></span>

```
Get-AzPrivateDnsZone [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="edad8-105">描述</span><span class="sxs-lookup"><span data-stu-id="edad8-105">DESCRIPTION</span></span>
<span data-ttu-id="edad8-106">**Get-AzPrivateDnsZone Cmdlet** 會從指定的資源群組 (DNS) 區域取得私人網域名稱系統。</span><span class="sxs-lookup"><span data-stu-id="edad8-106">The **Get-AzPrivateDnsZone** cmdlet gets a Private Domain Name System (DNS) zone from the specified resource group.</span></span>
<span data-ttu-id="edad8-107">如果您指定 *Name* 參數，會返回單 **一 PrivateDnsZone** 物件。</span><span class="sxs-lookup"><span data-stu-id="edad8-107">If you specify the *Name* parameter, a single **PrivateDnsZone** object is returned.</span></span>
<span data-ttu-id="edad8-108">如果您未指定 *Name* 參數，則包含指定資源群組中所有區域之陣列會返回。</span><span class="sxs-lookup"><span data-stu-id="edad8-108">If you do not specify the *Name* parameter, an array containing all of the zones in the specified resource group is returned.</span></span>
<span data-ttu-id="edad8-109">您可以使用 **PrivateDnsZone 物件** 來更新區域，例如，您可以新增 **RecordSet** 物件至該區域。</span><span class="sxs-lookup"><span data-stu-id="edad8-109">You can use the **PrivateDnsZone** object to update the zone, for example you can add **RecordSet** objects to it.</span></span>

## <span data-ttu-id="edad8-110">例子</span><span class="sxs-lookup"><span data-stu-id="edad8-110">EXAMPLES</span></span>

### <span data-ttu-id="edad8-111">範例 1：取得區域</span><span class="sxs-lookup"><span data-stu-id="edad8-111">Example 1: Get a zone</span></span>
```
PS C:\> $Zone = Get-AzPrivateDnsZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com"

This example gets the Private DNS zone named myzone.com from the specified resource group, and then stores it in the $Zone variable.
$Zone looks something like this: 

Name                          : myzone.com
ResourceId:                   : "/subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/PrivateZones/myzone.com"
ResourceGroupName             : MyResourceGroup
Location                      : 
Etag                          : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Tags                          : {}
NumberOfRecordSets            : 1
MaxNumberOfRecordSets         : 5000
```

### <span data-ttu-id="edad8-112">範例 2：取得資源群組的所有區域</span><span class="sxs-lookup"><span data-stu-id="edad8-112">Example 2: Get all of the zones in a resource group</span></span>
```
PS C:\> $Zones = Get-AzPrivateDnsZone -ResourceGroupName "MyResourceGroup"

Name                  : zone1.com
ResourceId            : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Micros
                        oft.Network/privateDnsZones/zone1.com
ResourceGroupName     : MyResourceGroup
Location              :
Etag                  : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Tags                  :
NumberOfRecordSets    : 1
MaxNumberOfRecordSets : 5000

Name                  : zone2.com
ResourceId            : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Micros
                        oft.Network/privateDnsZones/zone2.com
ResourceGroupName     : MyResourceGroup
Location              :
Etag                  : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Tags                  :
NumberOfRecordSets    : 1
MaxNumberOfRecordSets : 5000
```

<span data-ttu-id="edad8-113">此範例會獲得指定資源群組中所有的私人 DNS 區域，然後將它儲存在 $Zones 變數中。</span><span class="sxs-lookup"><span data-stu-id="edad8-113">This example gets all of the Private DNS zones in the specified resource group, and then stores it in the $Zones variable.</span></span>

### <span data-ttu-id="edad8-114">範例 3：取得訂閱的所有區域</span><span class="sxs-lookup"><span data-stu-id="edad8-114">Example 3: Get all of the zones in a subscription</span></span>
```
PS C:\> $Zones = Get-AzPrivateDnsZone

Name                  : zone1.com
ResourceId            : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup1/providers/Micros
                        oft.Network/privateDnsZones/zone1.com
ResourceGroupName     : MyResourceGroup1
Location              :
Etag                  : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Tags                  :
NumberOfRecordSets    : 1
MaxNumberOfRecordSets : 5000

Name                  : zone2.com
ResourceId            : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup2/providers/Micros
                        oft.Network/privateDnsZones/zone2.com
ResourceGroupName     : MyResourceGroup2
Location              :
Etag                  : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Tags                  :
NumberOfRecordSets    : 1
MaxNumberOfRecordSets : 5000
```

<span data-ttu-id="edad8-115">此範例會獲得目前 Azure 訂閱中所有的私人 DNS 區域，然後將它們儲存在 $Zones 變數中。</span><span class="sxs-lookup"><span data-stu-id="edad8-115">This example gets all of the Private DNS zones in the current Azure subscription, and then stores them in the $Zones variable.</span></span>

## <span data-ttu-id="edad8-116">參數</span><span class="sxs-lookup"><span data-stu-id="edad8-116">PARAMETERS</span></span>

### <span data-ttu-id="edad8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edad8-117">-DefaultProfile</span></span>
<span data-ttu-id="edad8-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="edad8-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="edad8-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="edad8-119">-Name</span></span>
<span data-ttu-id="edad8-120">指定要取得的私人 DNS 區功能變數名稱稱。</span><span class="sxs-lookup"><span data-stu-id="edad8-120">Specifies the name of the Private DNS zone to get.</span></span>
<span data-ttu-id="edad8-121">如果您未指定 Name 參數的值，此Cmdlet 會獲得指定資源群組中所有的私人 DNS 區域。</span><span class="sxs-lookup"><span data-stu-id="edad8-121">If you do not specify a value for the *Name* parameter, this cmdlet gets all Private DNS zones in the specified resource group.</span></span>
<span data-ttu-id="edad8-122">如果您也省略 *ResourceGroupName* 參數，此 Cmdlet 會獲得目前 Azure 訂閱中所有的私人 DNS 區域。</span><span class="sxs-lookup"><span data-stu-id="edad8-122">If you also omit the *ResourceGroupName* parameter, this cmdlet gets all Private DNS zones in the current Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edad8-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="edad8-123">-ResourceGroupName</span></span>
<span data-ttu-id="edad8-124">指定包含要取得之私人 DNS 區域的資源組名。</span><span class="sxs-lookup"><span data-stu-id="edad8-124">Specifies the name of the resource group that contains the Private DNS zone to get.</span></span>
<span data-ttu-id="edad8-125">如果您未指定 *ResourceGroupName，* 則也必須省略 *Name* 參數。</span><span class="sxs-lookup"><span data-stu-id="edad8-125">If you do not specify the *ResourceGroupName*, then you must also omit the *Name* parameter.</span></span>
<span data-ttu-id="edad8-126">在此案例中，此 Cmdlet 會獲得目前 Azure 訂閱中所有的私人 DNS 區域。</span><span class="sxs-lookup"><span data-stu-id="edad8-126">In this case, this cmdlet gets all Private DNS zones in the current Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edad8-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edad8-127">CommonParameters</span></span>
<span data-ttu-id="edad8-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="edad8-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edad8-129">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="edad8-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edad8-130">輸入</span><span class="sxs-lookup"><span data-stu-id="edad8-130">INPUTS</span></span>

### <span data-ttu-id="edad8-131">沒有</span><span class="sxs-lookup"><span data-stu-id="edad8-131">None</span></span>

## <span data-ttu-id="edad8-132">輸出</span><span class="sxs-lookup"><span data-stu-id="edad8-132">OUTPUTS</span></span>

### <span data-ttu-id="edad8-133">Microsoft.Azure.Commands.PrivateDns.models.PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="edad8-133">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

## <span data-ttu-id="edad8-134">筆記</span><span class="sxs-lookup"><span data-stu-id="edad8-134">NOTES</span></span>

## <span data-ttu-id="edad8-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="edad8-135">RELATED LINKS</span></span>

[<span data-ttu-id="edad8-136">New-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="edad8-136">New-AzPrivateDnsZone</span></span>](./New-AzPrivateDnsZone.md)

[<span data-ttu-id="edad8-137">Remove-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="edad8-137">Remove-AzPrivateDnsZone</span></span>](./Remove-AzPrivateDnsZone.md)

[<span data-ttu-id="edad8-138">Set-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="edad8-138">Set-AzPrivateDnsZone</span></span>](./Set-AzPrivateDnsZone.md)
