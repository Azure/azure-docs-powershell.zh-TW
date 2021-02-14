---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotCentral.dll-Help.xml
Module Name: Az.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/az.iotcentral/get-aziotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Get-AzIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Get-AzIotCentralApp.md
ms.openlocfilehash: cbc7e255f74943ea2aff3518d278035f72394235
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100140811"
---
# <span data-ttu-id="d1666-101">Get-AzIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="d1666-101">Get-AzIotCentralApp</span></span>

## <span data-ttu-id="d1666-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d1666-102">SYNOPSIS</span></span>
<span data-ttu-id="d1666-103">取得一或多個 IoT 中央應用程式的屬性。</span><span class="sxs-lookup"><span data-stu-id="d1666-103">Gets properties for either one or several IoT Central Applications.</span></span>

## <span data-ttu-id="d1666-104">句法</span><span class="sxs-lookup"><span data-stu-id="d1666-104">SYNTAX</span></span>

### <span data-ttu-id="d1666-105">ListIotCentralAppsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="d1666-105">ListIotCentralAppsParameterSet (Default)</span></span>
```
Get-AzIotCentralApp [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d1666-106">InteractiveIotCentralParameterSet</span><span class="sxs-lookup"><span data-stu-id="d1666-106">InteractiveIotCentralParameterSet</span></span>
```
Get-AzIotCentralApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d1666-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d1666-107">ResourceIdParameterSet</span></span>
```
Get-AzIotCentralApp -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d1666-108">說明</span><span class="sxs-lookup"><span data-stu-id="d1666-108">DESCRIPTION</span></span>
<span data-ttu-id="d1666-109">根據參數集，取得特定 IoT 中央應用程式的中繼資料，或是資源群組或訂閱中的所有應用程式。</span><span class="sxs-lookup"><span data-stu-id="d1666-109">Gets the metadata for either a specific IoT Central Application, or all the applications in a Resource Group or Subscription, depending on Parameter Set.</span></span> 

## <span data-ttu-id="d1666-110">示例</span><span class="sxs-lookup"><span data-stu-id="d1666-110">EXAMPLES</span></span>

### <span data-ttu-id="d1666-111">範例1取得特定的 IoT 中央應用程式。</span><span class="sxs-lookup"><span data-stu-id="d1666-111">Example 1 Get Specific IoT Central Application.</span></span>
```powershell
PS C:\> Get-AzIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName"
```

<span data-ttu-id="d1666-112">取得指定 IoT 中央應用程式的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="d1666-112">Gets the metadata for the specified IoT Central Application.</span></span>

<span data-ttu-id="d1666-113">範例輸出：</span><span class="sxs-lookup"><span data-stu-id="d1666-113">Example Output:</span></span>

<span data-ttu-id="d1666-114">ResourceId：/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft。IoTCentral/IoTApps/MyAppResourceName 名稱： MyAppResourceName 類型： Microsoft. IoTCentral/IoTApps Location： westus 標記： {[key，val]} Sku： ApplicationId： XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName： [我的自訂顯示名稱子域： IoTCentral 範本： iotc-default@1.0.0 ： xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx-Xxxx PSIotCentralAppSkuInfo： MyAppSubdomain （不適用）</span><span class="sxs-lookup"><span data-stu-id="d1666-114">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

### <span data-ttu-id="d1666-115">範例2在訂閱中取得 IoT 中央應用程式。</span><span class="sxs-lookup"><span data-stu-id="d1666-115">Example 2 Get IoT Central Applications in Subscription.</span></span>
```powershell
PS C:\> Get-AzIotCentralApp
```

<span data-ttu-id="d1666-116">取得目前訂閱中所有 IoT 中央應用程式的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="d1666-116">Gets the metadata for all the IoT Central Applications in the current Subscription.</span></span>

<span data-ttu-id="d1666-117">範例輸出：</span><span class="sxs-lookup"><span data-stu-id="d1666-117">Example Output:</span></span>

<span data-ttu-id="d1666-118">ResourceId：/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft。IoTCentral/IoTApps/MyAppResourceName 名稱： MyAppResourceName 類型： Microsoft. IoTCentral/IoTApps Location： westus 標記： {[key，val]} Sku： ApplicationId： XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName： [我的自訂顯示名稱子域： IoTCentral 範本： iotc-default@1.0.0 ： xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx-Xxxx PSIotCentralAppSkuInfo： MyAppSubdomain （不適用）</span><span class="sxs-lookup"><span data-stu-id="d1666-118">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

<span data-ttu-id="d1666-119">ResourceId：/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName2/providers/Microsoft。IoTCentral/IoTApps/MyAppResourceName2 名稱： MyAppResourceName2 類型： Microsoft. IoTCentral/IoTApps Location： westus 標記： {[key，val]} Sku：： ApplicationId： XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName： [我的自訂顯示名稱2子域： IoTCentral 範本： iotc-default@1.0.0 訂閱： xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx-Xxxx PSIotCentralAppSkuInfo： MyAppSubdomain2</span><span class="sxs-lookup"><span data-stu-id="d1666-119">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName2/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName2 Name              : MyAppResourceName2 Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name 2 Subdomain         : MyAppSubdomain2 Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName2</span></span>

### <span data-ttu-id="d1666-120">範例3在 [資源群組] 中取得 IoT 中央應用程式。</span><span class="sxs-lookup"><span data-stu-id="d1666-120">Example 3 Get IoT Central Applications in Resource Group.</span></span>
```powershell
PS C:\> Get-AzIotCentralApp -ResourceGroupName "MyResourceGroupName"
```

<span data-ttu-id="d1666-121">取得所提供之資源群組中所有 IoT 中心應用程式的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="d1666-121">Gets the metadata for all IoT Central Applications in the provided Resource Group.</span></span>

<span data-ttu-id="d1666-122">範例輸出：</span><span class="sxs-lookup"><span data-stu-id="d1666-122">Example Output:</span></span>

<span data-ttu-id="d1666-123">ResourceId：/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft。IoTCentral/IoTApps/MyAppResourceName 名稱： MyAppResourceName 類型： Microsoft. IoTCentral/IoTApps Location： westus 標記： {[key，val]} Sku： ApplicationId： XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName： [我的自訂顯示名稱子域： IoTCentral 範本： iotc-default@1.0.0 ： xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx-Xxxx PSIotCentralAppSkuInfo： MyAppSubdomain （不適用）</span><span class="sxs-lookup"><span data-stu-id="d1666-123">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

<span data-ttu-id="d1666-124">ResourceId：/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft。IoTCentral/IoTApps/MyAppResourceName2 名稱： MyAppResourceName2 類型： Microsoft. IoTCentral/IoTApps Location： westus 標記： {[key，val]} Sku：： ApplicationId： XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName： [我的自訂顯示名稱2子域： IoTCentral 範本： iotc-default@1.0.0 訂閱： xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx-Xxxx PSIotCentralAppSkuInfo： MyAppSubdomain2</span><span class="sxs-lookup"><span data-stu-id="d1666-124">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName2 Name              : MyAppResourceName2 Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name 2 Subdomain         : MyAppSubdomain2 Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

## <span data-ttu-id="d1666-125">參數</span><span class="sxs-lookup"><span data-stu-id="d1666-125">PARAMETERS</span></span>

### <span data-ttu-id="d1666-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1666-126">-DefaultProfile</span></span>
<span data-ttu-id="d1666-127">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d1666-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1666-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="d1666-128">-Name</span></span>
<span data-ttu-id="d1666-129">Iot 中心應用程式資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="d1666-129">Name of the Iot Central Application Resource.</span></span>

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

### <span data-ttu-id="d1666-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1666-130">-ResourceGroupName</span></span>
<span data-ttu-id="d1666-131">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d1666-131">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="d1666-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d1666-132">-ResourceId</span></span>
<span data-ttu-id="d1666-133">Iot 中心應用程式資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="d1666-133">Iot Central Application Resource Id.</span></span>

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

### <span data-ttu-id="d1666-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1666-134">CommonParameters</span></span>
<span data-ttu-id="d1666-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d1666-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1666-136">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="d1666-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1666-137">輸入</span><span class="sxs-lookup"><span data-stu-id="d1666-137">INPUTS</span></span>

### <span data-ttu-id="d1666-138">System.object</span><span class="sxs-lookup"><span data-stu-id="d1666-138">System.String</span></span>

## <span data-ttu-id="d1666-139">輸出</span><span class="sxs-lookup"><span data-stu-id="d1666-139">OUTPUTS</span></span>

### <span data-ttu-id="d1666-140">PSIotCentralApp 中的 IotCentral。</span><span class="sxs-lookup"><span data-stu-id="d1666-140">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="d1666-141">筆記</span><span class="sxs-lookup"><span data-stu-id="d1666-141">NOTES</span></span>

## <span data-ttu-id="d1666-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="d1666-142">RELATED LINKS</span></span>
