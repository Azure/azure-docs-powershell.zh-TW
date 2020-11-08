---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/get-azprivatednszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Get-AzPrivateDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Get-AzPrivateDnsZone.md
ms.openlocfilehash: 3a909bcae464c70487ce4705bfaa43336776472b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94128857"
---
# <span data-ttu-id="f08ef-101">Get-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="f08ef-101">Get-AzPrivateDnsZone</span></span>

## <span data-ttu-id="f08ef-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f08ef-102">SYNOPSIS</span></span>
<span data-ttu-id="f08ef-103">取得私人 DNS 區域。</span><span class="sxs-lookup"><span data-stu-id="f08ef-103">Gets a Private DNS zone.</span></span>

## <span data-ttu-id="f08ef-104">句法</span><span class="sxs-lookup"><span data-stu-id="f08ef-104">SYNTAX</span></span>

```
Get-AzPrivateDnsZone [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f08ef-105">說明</span><span class="sxs-lookup"><span data-stu-id="f08ef-105">DESCRIPTION</span></span>
<span data-ttu-id="f08ef-106">**AzPrivateDnsZone** Cmdlet 會從指定的資源群組 (DNS) 區域中取得私人網功能變數名稱稱系統。</span><span class="sxs-lookup"><span data-stu-id="f08ef-106">The **Get-AzPrivateDnsZone** cmdlet gets a Private Domain Name System (DNS) zone from the specified resource group.</span></span>
<span data-ttu-id="f08ef-107">如果您指定 *Name* 參數，則會傳回單一 **PrivateDnsZone** 物件。</span><span class="sxs-lookup"><span data-stu-id="f08ef-107">If you specify the *Name* parameter, a single **PrivateDnsZone** object is returned.</span></span>
<span data-ttu-id="f08ef-108">如果您沒有指定 *Name* 參數，則會傳回包含指定資源群組中所有區域的陣列。</span><span class="sxs-lookup"><span data-stu-id="f08ef-108">If you do not specify the *Name* parameter, an array containing all of the zones in the specified resource group is returned.</span></span>
<span data-ttu-id="f08ef-109">您可以使用 **PrivateDnsZone** 物件來更新區域，例如，您可以將 **記錄集** 物件新增到其中。</span><span class="sxs-lookup"><span data-stu-id="f08ef-109">You can use the **PrivateDnsZone** object to update the zone, for example you can add **RecordSet** objects to it.</span></span>

## <span data-ttu-id="f08ef-110">示例</span><span class="sxs-lookup"><span data-stu-id="f08ef-110">EXAMPLES</span></span>

### <span data-ttu-id="f08ef-111">範例1：取得區域</span><span class="sxs-lookup"><span data-stu-id="f08ef-111">Example 1: Get a zone</span></span>
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

### <span data-ttu-id="f08ef-112">範例2：取得資源群組中的所有區域</span><span class="sxs-lookup"><span data-stu-id="f08ef-112">Example 2: Get all of the zones in a resource group</span></span>
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

<span data-ttu-id="f08ef-113">這個範例會取得指定資源群組中的所有私人 DNS 區域，然後將它儲存在 $Zones 變數中。</span><span class="sxs-lookup"><span data-stu-id="f08ef-113">This example gets all of the Private DNS zones in the specified resource group, and then stores it in the $Zones variable.</span></span>

### <span data-ttu-id="f08ef-114">範例3：取得訂閱中的所有區域</span><span class="sxs-lookup"><span data-stu-id="f08ef-114">Example 3: Get all of the zones in a subscription</span></span>
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

<span data-ttu-id="f08ef-115">這個範例會取得目前 Azure 訂閱中的所有私人 DNS 區域，然後將它們儲存在 $Zones 變數中。</span><span class="sxs-lookup"><span data-stu-id="f08ef-115">This example gets all of the Private DNS zones in the current Azure subscription, and then stores them in the $Zones variable.</span></span>

## <span data-ttu-id="f08ef-116">參數</span><span class="sxs-lookup"><span data-stu-id="f08ef-116">PARAMETERS</span></span>

### <span data-ttu-id="f08ef-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f08ef-117">-DefaultProfile</span></span>
<span data-ttu-id="f08ef-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="f08ef-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f08ef-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="f08ef-119">-Name</span></span>
<span data-ttu-id="f08ef-120">指定要取得的專用 DNS 區域的名稱。</span><span class="sxs-lookup"><span data-stu-id="f08ef-120">Specifies the name of the Private DNS zone to get.</span></span>
<span data-ttu-id="f08ef-121">如果您沒有指定 *Name* 參數的值，這個 Cmdlet 會取得指定資源群組中的所有私人 DNS 區域。</span><span class="sxs-lookup"><span data-stu-id="f08ef-121">If you do not specify a value for the *Name* parameter, this cmdlet gets all Private DNS zones in the specified resource group.</span></span>
<span data-ttu-id="f08ef-122">如果您也省略 *ResourceGroupName* 參數，這個 Cmdlet 會取得目前 Azure 訂閱中的所有私人 DNS 區域。</span><span class="sxs-lookup"><span data-stu-id="f08ef-122">If you also omit the *ResourceGroupName* parameter, this cmdlet gets all Private DNS zones in the current Azure subscription.</span></span>

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

### <span data-ttu-id="f08ef-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f08ef-123">-ResourceGroupName</span></span>
<span data-ttu-id="f08ef-124">指定包含要取得的私人 DNS 區域的資源群組名稱。</span><span class="sxs-lookup"><span data-stu-id="f08ef-124">Specifies the name of the resource group that contains the Private DNS zone to get.</span></span>
<span data-ttu-id="f08ef-125">如果您沒有指定 *ResourceGroupName* ，則您也必須省略 *Name* 參數。</span><span class="sxs-lookup"><span data-stu-id="f08ef-125">If you do not specify the *ResourceGroupName* , then you must also omit the *Name* parameter.</span></span>
<span data-ttu-id="f08ef-126">在這種情況下，這個 Cmdlet 會取得目前 Azure 訂閱中的所有私人 DNS 區域。</span><span class="sxs-lookup"><span data-stu-id="f08ef-126">In this case, this cmdlet gets all Private DNS zones in the current Azure subscription.</span></span>

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

### <span data-ttu-id="f08ef-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f08ef-127">CommonParameters</span></span>
<span data-ttu-id="f08ef-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f08ef-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f08ef-129">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f08ef-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f08ef-130">輸入</span><span class="sxs-lookup"><span data-stu-id="f08ef-130">INPUTS</span></span>

### <span data-ttu-id="f08ef-131">所有</span><span class="sxs-lookup"><span data-stu-id="f08ef-131">None</span></span>

## <span data-ttu-id="f08ef-132">輸出</span><span class="sxs-lookup"><span data-stu-id="f08ef-132">OUTPUTS</span></span>

### <span data-ttu-id="f08ef-133">PSPrivateDnsZone 中的 PrivateDns。</span><span class="sxs-lookup"><span data-stu-id="f08ef-133">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

## <span data-ttu-id="f08ef-134">筆記</span><span class="sxs-lookup"><span data-stu-id="f08ef-134">NOTES</span></span>

## <span data-ttu-id="f08ef-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="f08ef-135">RELATED LINKS</span></span>

[<span data-ttu-id="f08ef-136">新-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="f08ef-136">New-AzPrivateDnsZone</span></span>](./New-AzPrivateDnsZone.md)

[<span data-ttu-id="f08ef-137">移除-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="f08ef-137">Remove-AzPrivateDnsZone</span></span>](./Remove-AzPrivateDnsZone.md)

[<span data-ttu-id="f08ef-138">Set-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="f08ef-138">Set-AzPrivateDnsZone</span></span>](./Set-AzPrivateDnsZone.md)
