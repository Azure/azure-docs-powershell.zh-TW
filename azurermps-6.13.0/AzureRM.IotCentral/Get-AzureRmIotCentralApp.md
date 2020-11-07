---
external help file: Microsoft.Azure.Commands.IotCentral.dll-Help.xml
Module Name: AzureRM.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iotcentral/get-azurermiotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotCentral/Commands.IotCentral/help/Get-AzureRmIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotCentral/Commands.IotCentral/help/Get-AzureRmIotCentralApp.md
ms.openlocfilehash: fdf674b5ec2dfcefe8fcada92cfaf0fd1073f7f3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626401"
---
# <span data-ttu-id="91600-101">Get-AzureRmIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="91600-101">Get-AzureRmIotCentralApp</span></span>

## <span data-ttu-id="91600-102">摘要</span><span class="sxs-lookup"><span data-stu-id="91600-102">SYNOPSIS</span></span>
<span data-ttu-id="91600-103">取得一或多個 IoT 中央應用程式的屬性。</span><span class="sxs-lookup"><span data-stu-id="91600-103">Gets properties for either one or several IoT Central Applications.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="91600-104">句法</span><span class="sxs-lookup"><span data-stu-id="91600-104">SYNTAX</span></span>

### <span data-ttu-id="91600-105">ListIotCentralAppsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="91600-105">ListIotCentralAppsParameterSet (Default)</span></span>
```
Get-AzureRmIotCentralApp [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="91600-106">InteractiveIotCentralParameterSet</span><span class="sxs-lookup"><span data-stu-id="91600-106">InteractiveIotCentralParameterSet</span></span>
```
Get-AzureRmIotCentralApp [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="91600-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="91600-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmIotCentralApp -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="91600-108">說明</span><span class="sxs-lookup"><span data-stu-id="91600-108">DESCRIPTION</span></span>
<span data-ttu-id="91600-109">根據參數集，取得特定 IoT 中央應用程式的中繼資料，或是資源群組或訂閱中的所有應用程式。</span><span class="sxs-lookup"><span data-stu-id="91600-109">Gets the metadata for either a specific IoT Central Application, or all the applications in a Resource Group or Subscription, depending on Parameter Set.</span></span> 

## <span data-ttu-id="91600-110">示例</span><span class="sxs-lookup"><span data-stu-id="91600-110">EXAMPLES</span></span>

### <span data-ttu-id="91600-111">範例1取得特定的 IoT 中央應用程式。</span><span class="sxs-lookup"><span data-stu-id="91600-111">Example 1 Get Specific IoT Central Application.</span></span>
```powershell
PS C:\> Get-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName"
```

<span data-ttu-id="91600-112">取得指定 IoT 中央應用程式的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="91600-112">Gets the metadata for the specified IoT Central Application.</span></span>

<span data-ttu-id="91600-113">範例輸出：</span><span class="sxs-lookup"><span data-stu-id="91600-113">Example Output:</span></span>

<span data-ttu-id="91600-114">ResourceId：/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft。IoTCentral/IoTApps/MyAppResourceName 名稱： MyAppResourceName 類型： Microsoft. IoTCentral/IoTApps Location： westus 標記： {[key，val]} Sku： ApplicationId： XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName： [我的自訂顯示名稱子域： IoTCentral 範本： iotc-default@1.0.0 ： xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx-Xxxx PSIotCentralAppSkuInfo： MyAppSubdomain （不適用）</span><span class="sxs-lookup"><span data-stu-id="91600-114">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

### <span data-ttu-id="91600-115">範例2在訂閱中取得 IoT 中央應用程式。</span><span class="sxs-lookup"><span data-stu-id="91600-115">Example 2 Get IoT Central Applications in Subscription.</span></span>
```powershell
PS C:\> Get-AzureRmIotCentralApp
```

<span data-ttu-id="91600-116">取得目前訂閱中所有 IoT 中央應用程式的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="91600-116">Gets the metadata for all the IoT Central Applications in the current Subscription.</span></span>

<span data-ttu-id="91600-117">範例輸出：</span><span class="sxs-lookup"><span data-stu-id="91600-117">Example Output:</span></span>

<span data-ttu-id="91600-118">ResourceId：/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft。IoTCentral/IoTApps/MyAppResourceName 名稱： MyAppResourceName 類型： Microsoft. IoTCentral/IoTApps Location： westus 標記： {[key，val]} Sku： ApplicationId： XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName： [我的自訂顯示名稱子域： IoTCentral 範本： iotc-default@1.0.0 ： xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx-Xxxx PSIotCentralAppSkuInfo： MyAppSubdomain （不適用）</span><span class="sxs-lookup"><span data-stu-id="91600-118">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

<span data-ttu-id="91600-119">ResourceId：/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName2/providers/Microsoft。IoTCentral/IoTApps/MyAppResourceName2 名稱： MyAppResourceName2 類型： Microsoft. IoTCentral/IoTApps Location： westus 標記： {[key，val]} Sku：： ApplicationId： XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName： [我的自訂顯示名稱2子域： IoTCentral 範本： iotc-default@1.0.0 訂閱： xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx-Xxxx PSIotCentralAppSkuInfo： MyAppSubdomain2</span><span class="sxs-lookup"><span data-stu-id="91600-119">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName2/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName2 Name              : MyAppResourceName2 Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name 2 Subdomain         : MyAppSubdomain2 Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName2</span></span>

### <span data-ttu-id="91600-120">範例3在 [資源群組] 中取得 IoT 中央應用程式。</span><span class="sxs-lookup"><span data-stu-id="91600-120">Example 3 Get IoT Central Applications in Resource Group.</span></span>
```powershell
PS C:\> Get-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName"
```

<span data-ttu-id="91600-121">取得所提供之資源群組中所有 IoT 中心應用程式的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="91600-121">Gets the metadata for all IoT Central Applications in the provided Resource Group.</span></span>

<span data-ttu-id="91600-122">範例輸出：</span><span class="sxs-lookup"><span data-stu-id="91600-122">Example Output:</span></span>

<span data-ttu-id="91600-123">ResourceId：/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft。IoTCentral/IoTApps/MyAppResourceName 名稱： MyAppResourceName 類型： Microsoft. IoTCentral/IoTApps Location： westus 標記： {[key，val]} Sku： ApplicationId： XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName： [我的自訂顯示名稱子域： IoTCentral 範本： iotc-default@1.0.0 ： xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx-Xxxx PSIotCentralAppSkuInfo： MyAppSubdomain （不適用）</span><span class="sxs-lookup"><span data-stu-id="91600-123">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

<span data-ttu-id="91600-124">ResourceId：/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft。IoTCentral/IoTApps/MyAppResourceName2 名稱： MyAppResourceName2 類型： Microsoft. IoTCentral/IoTApps Location： westus 標記： {[key，val]} Sku：： ApplicationId： XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName： [我的自訂顯示名稱2子域： IoTCentral 範本： iotc-default@1.0.0 訂閱： xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx-Xxxx PSIotCentralAppSkuInfo： MyAppSubdomain2</span><span class="sxs-lookup"><span data-stu-id="91600-124">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName2 Name              : MyAppResourceName2 Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name 2 Subdomain         : MyAppSubdomain2 Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

## <span data-ttu-id="91600-125">參數</span><span class="sxs-lookup"><span data-stu-id="91600-125">PARAMETERS</span></span>

### <span data-ttu-id="91600-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91600-126">-DefaultProfile</span></span>
<span data-ttu-id="91600-127">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="91600-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91600-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="91600-128">-Name</span></span>
<span data-ttu-id="91600-129">Iot 中心應用程式資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="91600-129">Name of the Iot Central Application Resource.</span></span>

```yaml
Type: String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91600-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91600-130">-ResourceGroupName</span></span>
<span data-ttu-id="91600-131">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="91600-131">Name of the Resource Group.</span></span>

```yaml
Type: String
Parameter Sets: ListIotCentralAppsParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91600-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="91600-132">-ResourceId</span></span>
<span data-ttu-id="91600-133">Iot 中心應用程式資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="91600-133">Iot Central Application Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91600-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91600-134">CommonParameters</span></span>
<span data-ttu-id="91600-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="91600-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91600-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="91600-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91600-137">輸入</span><span class="sxs-lookup"><span data-stu-id="91600-137">INPUTS</span></span>

### <span data-ttu-id="91600-138">System.object</span><span class="sxs-lookup"><span data-stu-id="91600-138">System.String</span></span>
## <span data-ttu-id="91600-139">輸出</span><span class="sxs-lookup"><span data-stu-id="91600-139">OUTPUTS</span></span>

### <span data-ttu-id="91600-140">PSIotCentralApp 中的 IotCentral。</span><span class="sxs-lookup"><span data-stu-id="91600-140">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>
## <span data-ttu-id="91600-141">筆記</span><span class="sxs-lookup"><span data-stu-id="91600-141">NOTES</span></span>

## <span data-ttu-id="91600-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="91600-142">RELATED LINKS</span></span>
