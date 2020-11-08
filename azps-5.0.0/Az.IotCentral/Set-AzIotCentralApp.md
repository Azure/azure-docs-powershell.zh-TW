---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotCentral.dll-Help.xml
Module Name: Az.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/az.iotcentral/set-aziotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Set-AzIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Set-AzIotCentralApp.md
ms.openlocfilehash: 94a6e4d2b140487b279d85db1a8b663e03523ce4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94139240"
---
# <span data-ttu-id="25b0e-101">Set-AzIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="25b0e-101">Set-AzIotCentralApp</span></span>

## <span data-ttu-id="25b0e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="25b0e-102">SYNOPSIS</span></span>
<span data-ttu-id="25b0e-103">更新 IoT 中央應用程式的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="25b0e-103">Updates the metadata for an IoT Central Application.</span></span>

## <span data-ttu-id="25b0e-104">句法</span><span class="sxs-lookup"><span data-stu-id="25b0e-104">SYNTAX</span></span>

### <span data-ttu-id="25b0e-105">ResourceIdParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="25b0e-105">ResourceIdParameterSet (Default)</span></span>
```
Set-AzIotCentralApp [-DisplayName <String>] [-Subdomain <String>] [-Tag <Hashtable>] [-Sku <String>]
 -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="25b0e-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="25b0e-106">InputObjectParameterSet</span></span>
```
Set-AzIotCentralApp [-DisplayName <String>] [-Subdomain <String>] [-Tag <Hashtable>] [-Sku <String>]
 -InputObject <PSIotCentralApp> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="25b0e-107">InteractiveIotCentralParameterSet</span><span class="sxs-lookup"><span data-stu-id="25b0e-107">InteractiveIotCentralParameterSet</span></span>
```
Set-AzIotCentralApp [-DisplayName <String>] [-Subdomain <String>] [-Tag <Hashtable>] [-Sku <String>] [-AsJob]
 [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="25b0e-108">說明</span><span class="sxs-lookup"><span data-stu-id="25b0e-108">DESCRIPTION</span></span>
<span data-ttu-id="25b0e-109">更新 IoT 中央應用程式的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="25b0e-109">Update the metadata for an IoT Central Application.</span></span> 

## <span data-ttu-id="25b0e-110">示例</span><span class="sxs-lookup"><span data-stu-id="25b0e-110">EXAMPLES</span></span>

### <span data-ttu-id="25b0e-111">範例1更新顯示名稱</span><span class="sxs-lookup"><span data-stu-id="25b0e-111">Example 1 Update Display Name</span></span>
```powershell
PS C:\> Set-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -DisplayName "My New Custom Display Name"
```

<span data-ttu-id="25b0e-112">更新現有 IoT 中央應用程式的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="25b0e-112">Update the Display name on an existing IoT Central Application.</span></span>

<span data-ttu-id="25b0e-113">範例輸出：</span><span class="sxs-lookup"><span data-stu-id="25b0e-113">Example Output:</span></span>

<span data-ttu-id="25b0e-114">ResourceId：/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft。IoTCentral/IoTApps/MyAppResourceName 名稱： MyAppResourceName 類型：/IoTCentral 位置： IoTApps 標記： Sku：：的。 westus ApplicationId： [XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX]-xxxx xxxx：我的新自訂顯示名稱子域： IoTCentral 範本： iotc-default@1.0.0 SubscriptionId： xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx-Xxxx PSIotCentralAppSkuInfo： MyAppSubdomain</span><span class="sxs-lookup"><span data-stu-id="25b0e-114">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My New Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

### <span data-ttu-id="25b0e-115">範例2更新子域</span><span class="sxs-lookup"><span data-stu-id="25b0e-115">Example 2 Update Subdomain</span></span>
```powershell
PS C:\> Set-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Subdomain "new-subdomain"
```

<span data-ttu-id="25b0e-116">更新現有 IoT 中央應用程式的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="25b0e-116">Update the Display name on an existing IoT Central Application.</span></span>

<span data-ttu-id="25b0e-117">範例輸出：</span><span class="sxs-lookup"><span data-stu-id="25b0e-117">Example Output:</span></span>

<span data-ttu-id="25b0e-118">ResourceId：/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft。IoTCentral/IoTApps/MyAppResourceName 名稱： MyAppResourceName 類型：/IoTCentral 位置： IoTApps 標記： Sku：.. Westus. IoTCentral ApplicationId： [XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX 名稱] 子 DisplayName：顯示名稱子域：新的子域範本： SubscriptionId： [xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx]： [ iotc-default@1.0.0 PSIotCentralAppSkuInfo]</span><span class="sxs-lookup"><span data-stu-id="25b0e-118">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : Display Name Subdomain         : new-subdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

### <span data-ttu-id="25b0e-119">範例3更新應用程式 Sku 資訊</span><span class="sxs-lookup"><span data-stu-id="25b0e-119">Example 3 Update App Sku Info</span></span>
```powershell
PS C:\> Set-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Sku "ST2"
```

<span data-ttu-id="25b0e-120">在現有的 IoT 中央應用程式上更新 sku。</span><span class="sxs-lookup"><span data-stu-id="25b0e-120">Update the sku on an existing IoT Central Application.</span></span>

<span data-ttu-id="25b0e-121">範例輸出：</span><span class="sxs-lookup"><span data-stu-id="25b0e-121">Example Output:</span></span>

<span data-ttu-id="25b0e-122">ResourceId：/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft。IoTCentral/IoTApps/MyAppResourceName 名稱： MyAppResourceName 類型：/IoTCentral 位置： IoTApps 標記： Sku：.. Westus. IoTCentral ApplicationId： [XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX]-xxxx-xxxx DisplayName：顯示名稱子域： PSIotCentralAppSkuInfo 範本： iotc-default@1.0.0 SubscriptionId： Xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx MyAppSubdomain： ResourceGroupName。</span><span class="sxs-lookup"><span data-stu-id="25b0e-122">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

## <span data-ttu-id="25b0e-123">參數</span><span class="sxs-lookup"><span data-stu-id="25b0e-123">PARAMETERS</span></span>

### <span data-ttu-id="25b0e-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="25b0e-124">-AsJob</span></span>
<span data-ttu-id="25b0e-125">在背景中執行 Cmdlet 作為作業。</span><span class="sxs-lookup"><span data-stu-id="25b0e-125">Run cmdlet as a job in the background.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25b0e-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25b0e-126">-DefaultProfile</span></span>
<span data-ttu-id="25b0e-127">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="25b0e-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25b0e-128">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="25b0e-128">-DisplayName</span></span>
<span data-ttu-id="25b0e-129">Iot 中央應用程式的自訂顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="25b0e-129">Custom Display Name of the Iot Central Application.</span></span>

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

### <span data-ttu-id="25b0e-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="25b0e-130">-InputObject</span></span>
<span data-ttu-id="25b0e-131">Iot 中央應用程式輸入物件。</span><span class="sxs-lookup"><span data-stu-id="25b0e-131">Iot Central Application Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="25b0e-132">-名稱</span><span class="sxs-lookup"><span data-stu-id="25b0e-132">-Name</span></span>
<span data-ttu-id="25b0e-133">Iot 中心應用程式資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="25b0e-133">Name of the Iot Central Application Resource.</span></span>

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

### <span data-ttu-id="25b0e-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25b0e-134">-ResourceGroupName</span></span>
<span data-ttu-id="25b0e-135">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="25b0e-135">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="25b0e-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="25b0e-136">-ResourceId</span></span>
<span data-ttu-id="25b0e-137">Iot 中心應用程式資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="25b0e-137">Iot Central Application Resource Id.</span></span>

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

### <span data-ttu-id="25b0e-138">-Sku</span><span class="sxs-lookup"><span data-stu-id="25b0e-138">-Sku</span></span>
<span data-ttu-id="25b0e-139">IoT 中心應用程式的定價層。</span><span class="sxs-lookup"><span data-stu-id="25b0e-139">Pricing tier for IoT Central applications.</span></span>
<span data-ttu-id="25b0e-140">預設值為 ST2。</span><span class="sxs-lookup"><span data-stu-id="25b0e-140">Default value is ST2.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25b0e-141">-子域</span><span class="sxs-lookup"><span data-stu-id="25b0e-141">-Subdomain</span></span>
<span data-ttu-id="25b0e-142">IoT 中央應用程式的子域。</span><span class="sxs-lookup"><span data-stu-id="25b0e-142">Subdomain of the IoT Central Application.</span></span>

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

### <span data-ttu-id="25b0e-143">-Tag</span><span class="sxs-lookup"><span data-stu-id="25b0e-143">-Tag</span></span>
<span data-ttu-id="25b0e-144">Iot 中心應用程式資源標記。</span><span class="sxs-lookup"><span data-stu-id="25b0e-144">Iot Central Application Resource Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25b0e-145">-確認</span><span class="sxs-lookup"><span data-stu-id="25b0e-145">-Confirm</span></span>
<span data-ttu-id="25b0e-146">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="25b0e-146">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25b0e-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25b0e-147">-WhatIf</span></span>
<span data-ttu-id="25b0e-148">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="25b0e-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25b0e-149">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="25b0e-149">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25b0e-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25b0e-150">CommonParameters</span></span>
<span data-ttu-id="25b0e-151">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="25b0e-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25b0e-152">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="25b0e-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25b0e-153">輸入</span><span class="sxs-lookup"><span data-stu-id="25b0e-153">INPUTS</span></span>

### <span data-ttu-id="25b0e-154">System.object</span><span class="sxs-lookup"><span data-stu-id="25b0e-154">System.String</span></span>

### <span data-ttu-id="25b0e-155">PSIotCentralApp 中的 IotCentral。</span><span class="sxs-lookup"><span data-stu-id="25b0e-155">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="25b0e-156">輸出</span><span class="sxs-lookup"><span data-stu-id="25b0e-156">OUTPUTS</span></span>

### <span data-ttu-id="25b0e-157">PSIotCentralApp 中的 IotCentral。</span><span class="sxs-lookup"><span data-stu-id="25b0e-157">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="25b0e-158">筆記</span><span class="sxs-lookup"><span data-stu-id="25b0e-158">NOTES</span></span>

## <span data-ttu-id="25b0e-159">相關連結</span><span class="sxs-lookup"><span data-stu-id="25b0e-159">RELATED LINKS</span></span>
