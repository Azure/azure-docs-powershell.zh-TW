---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotCentral.dll-Help.xml
Module Name: Az.IotCentral
online version: https://docs.microsoft.com/powershell/module/az.iotcentral/get-aziotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Get-AzIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Get-AzIotCentralApp.md
ms.openlocfilehash: 2d79857df255bb960c51b87c536013921f3b1c00
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913906"
---
# <span data-ttu-id="3914c-101">Get-AzIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="3914c-101">Get-AzIotCentralApp</span></span>

## <span data-ttu-id="3914c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="3914c-102">SYNOPSIS</span></span>
<span data-ttu-id="3914c-103">為一或多個 IoT 中心應用程式獲取屬性。</span><span class="sxs-lookup"><span data-stu-id="3914c-103">Gets properties for either one or several IoT Central Applications.</span></span>

## <span data-ttu-id="3914c-104">語法</span><span class="sxs-lookup"><span data-stu-id="3914c-104">SYNTAX</span></span>

### <span data-ttu-id="3914c-105">ListIotCentralAppsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="3914c-105">ListIotCentralAppsParameterSet (Default)</span></span>
```
Get-AzIotCentralApp [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3914c-106">InteractiveIotCentralParameterSet</span><span class="sxs-lookup"><span data-stu-id="3914c-106">InteractiveIotCentralParameterSet</span></span>
```
Get-AzIotCentralApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3914c-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3914c-107">ResourceIdParameterSet</span></span>
```
Get-AzIotCentralApp -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3914c-108">描述</span><span class="sxs-lookup"><span data-stu-id="3914c-108">DESCRIPTION</span></span>
<span data-ttu-id="3914c-109">根據參數集，為特定 IoT 中心應用程式或資源群組或訂閱內的所有應用程式獲取中繼資料。</span><span class="sxs-lookup"><span data-stu-id="3914c-109">Gets the metadata for either a specific IoT Central Application, or all the applications in a Resource Group or Subscription, depending on Parameter Set.</span></span> 

## <span data-ttu-id="3914c-110">例子</span><span class="sxs-lookup"><span data-stu-id="3914c-110">EXAMPLES</span></span>

### <span data-ttu-id="3914c-111">範例 1 取得特定的 IoT 中心應用程式。</span><span class="sxs-lookup"><span data-stu-id="3914c-111">Example 1 Get Specific IoT Central Application.</span></span>
```powershell
PS C:\> Get-AzIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName"
```

<span data-ttu-id="3914c-112">為指定的 IoT 中心應用程式獲取中繼資料。</span><span class="sxs-lookup"><span data-stu-id="3914c-112">Gets the metadata for the specified IoT Central Application.</span></span>

<span data-ttu-id="3914c-113">輸出範例：</span><span class="sxs-lookup"><span data-stu-id="3914c-113">Example Output:</span></span>

<span data-ttu-id="3914c-114">ResourceId ：/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name ： MyAppResourceName 類型 ： Microsoft.IoTCentral/IoTApps Location ： westus Tag ： {[key， val]} Sku ： Microsoft.Azure.Commands.IotCentral.models.PSIotCentralAppSkuInfo ApplicationId ： XXXXXXXX-XXXX-XXXX-XXXX-XXXX-XXXX-XXXXXXXXX DisplayName ： MyAppSubdomain 範本 ： iotc-default@1.0.0 SubscriptionId ： XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXX ResourceGroupName ： MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3914c-114">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

### <span data-ttu-id="3914c-115">範例 2 在訂閱中取得 IoT 中心應用程式。</span><span class="sxs-lookup"><span data-stu-id="3914c-115">Example 2 Get IoT Central Applications in Subscription.</span></span>
```powershell
PS C:\> Get-AzIotCentralApp
```

<span data-ttu-id="3914c-116">在目前的訂閱中，獲得所有 IoT 中心應用程式的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="3914c-116">Gets the metadata for all the IoT Central Applications in the current Subscription.</span></span>

<span data-ttu-id="3914c-117">輸出範例：</span><span class="sxs-lookup"><span data-stu-id="3914c-117">Example Output:</span></span>

<span data-ttu-id="3914c-118">ResourceId ：/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name ： MyAppResourceName 類型 ： Microsoft.IoTCentral/IoTApps Location ： westus Tag ： {[key， val]} Sku ： Microsoft.Azure.Commands.IotCentral.models.PSIotCentralAppSkuInfo ApplicationId ： XXXXXXXX-XXXX-XXXX-XXXX-XXXX-XXXX-XXXXXXXXX DisplayName ： MyAppSubdomain 範本 ： iotc-default@1.0.0 SubscriptionId ： XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXX ResourceGroupName ： MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3914c-118">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

<span data-ttu-id="3914c-119">ResourceId ：/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName2/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName2 名稱： MyAppResourceName2 類型： Microsoft.IoTCentral/IoTApps Location ： westus Tag ： {[key， val]} SKU ： Microsoft.Azure.Commands.IotCentral.models.PSIotCentralAppSkuInfo ApplicationId ： XXXXXXXX-XXXX-XXXX-XXXX-XXXX-XXXX-XXXXXXXXX DisplayName ： MyAppSubdomain2 範本 ： iotc-default@1.0.0 SubscriptionId ： XXXXXXXX-XXXX-XXXXXXXXX ResourceGroupName ： MyResourceGroupName2</span><span class="sxs-lookup"><span data-stu-id="3914c-119">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName2/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName2 Name              : MyAppResourceName2 Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name 2 Subdomain         : MyAppSubdomain2 Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName2</span></span>

### <span data-ttu-id="3914c-120">範例 3 在資源群組中取得 IoT 中心應用程式。</span><span class="sxs-lookup"><span data-stu-id="3914c-120">Example 3 Get IoT Central Applications in Resource Group.</span></span>
```powershell
PS C:\> Get-AzIotCentralApp -ResourceGroupName "MyResourceGroupName"
```

<span data-ttu-id="3914c-121">在提供的資源群組中，獲得所有 IoT 中心應用程式的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="3914c-121">Gets the metadata for all IoT Central Applications in the provided Resource Group.</span></span>

<span data-ttu-id="3914c-122">輸出範例：</span><span class="sxs-lookup"><span data-stu-id="3914c-122">Example Output:</span></span>

<span data-ttu-id="3914c-123">ResourceId ：/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name ： MyAppResourceName 類型 ： Microsoft.IoTCentral/IoTApps Location ： westus Tag ： {[key， val]} Sku ： Microsoft.Azure.Commands.IotCentral.models.PSIotCentralAppSkuInfo ApplicationId ： XXXXXXXX-XXXX-XXXX-XXXX-XXXX-XXXX-XXXXXXXXX DisplayName ： MyAppSubdomain 範本 ： iotc-default@1.0.0 SubscriptionId ： XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXX ResourceGroupName ： MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3914c-123">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

<span data-ttu-id="3914c-124">ResourceId ：/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName2 名稱： MyAppResourceName2 類型： Microsoft.IoTCentral/IoTApps Location ： westus Tag ： {[key， val]} Sku ： Microsoft.Azure.Commands.IotCentral.models.PSIotCentralAppSkuInfo ApplicationId ： XXXXXXXX-XXXX-XXXX-XXXX-XXXX-XXXX-XXXXXXXXX DisplayName ： MyAppSubdomain2 範本 ： iotc-default@1.0.0 SubscriptionId ： XXXXXXXX-XXXX-XXXXXXXXX ResourceGroupName ： MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3914c-124">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName2 Name              : MyAppResourceName2 Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name 2 Subdomain         : MyAppSubdomain2 Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

## <span data-ttu-id="3914c-125">參數</span><span class="sxs-lookup"><span data-stu-id="3914c-125">PARAMETERS</span></span>

### <span data-ttu-id="3914c-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3914c-126">-DefaultProfile</span></span>
<span data-ttu-id="3914c-127">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="3914c-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3914c-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="3914c-128">-Name</span></span>
<span data-ttu-id="3914c-129">Iot 中心應用程式資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="3914c-129">Name of the Iot Central Application Resource.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3914c-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3914c-130">-ResourceGroupName</span></span>
<span data-ttu-id="3914c-131">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3914c-131">Name of the Resource Group.</span></span>

```yaml
Type: System.String
Parameter Sets: ListIotCentralAppsParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3914c-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3914c-132">-ResourceId</span></span>
<span data-ttu-id="3914c-133">Iot Central Application Resource Id.</span><span class="sxs-lookup"><span data-stu-id="3914c-133">Iot Central Application Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3914c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3914c-134">CommonParameters</span></span>
<span data-ttu-id="3914c-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="3914c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3914c-136">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3914c-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3914c-137">輸入</span><span class="sxs-lookup"><span data-stu-id="3914c-137">INPUTS</span></span>

### <span data-ttu-id="3914c-138">System.String</span><span class="sxs-lookup"><span data-stu-id="3914c-138">System.String</span></span>

## <span data-ttu-id="3914c-139">輸出</span><span class="sxs-lookup"><span data-stu-id="3914c-139">OUTPUTS</span></span>

### <span data-ttu-id="3914c-140">Microsoft.Azure.Commands.IotCentral.models.PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="3914c-140">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="3914c-141">筆記</span><span class="sxs-lookup"><span data-stu-id="3914c-141">NOTES</span></span>

## <span data-ttu-id="3914c-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="3914c-142">RELATED LINKS</span></span>
