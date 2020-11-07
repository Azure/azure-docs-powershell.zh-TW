---
external help file: Microsoft.Azure.Commands.IotCentral.dll-Help.xml
Module Name: AzureRM.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iotcentral/set-azurermiotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotCentral/Commands.IotCentral/help/Set-AzureRmIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotCentral/Commands.IotCentral/help/Set-AzureRmIotCentralApp.md
ms.openlocfilehash: a9b7dbc962809288979f5293c14fd875081f48bc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626400"
---
# <span data-ttu-id="d0e8e-101">Set-AzureRmIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="d0e8e-101">Set-AzureRmIotCentralApp</span></span>

## <span data-ttu-id="d0e8e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d0e8e-102">SYNOPSIS</span></span>
<span data-ttu-id="d0e8e-103">更新 IoT 中央應用程式的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="d0e8e-103">Updates the metadata for an IoT Central Application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d0e8e-104">句法</span><span class="sxs-lookup"><span data-stu-id="d0e8e-104">SYNTAX</span></span>

### <span data-ttu-id="d0e8e-105">ResourceIdParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="d0e8e-105">ResourceIdParameterSet (Default)</span></span>
```
Set-AzureRmIotCentralApp [-DisplayName <String>] [-Tag <Hashtable>] -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0e8e-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d0e8e-106">InputObjectParameterSet</span></span>
```
Set-AzureRmIotCentralApp [-DisplayName <String>] [-Tag <Hashtable>] -InputObject <PSIotCentralApp> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0e8e-107">InteractiveIotCentralParameterSet</span><span class="sxs-lookup"><span data-stu-id="d0e8e-107">InteractiveIotCentralParameterSet</span></span>
```
Set-AzureRmIotCentralApp [-DisplayName <String>] [-Tag <Hashtable>] [-AsJob] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0e8e-108">說明</span><span class="sxs-lookup"><span data-stu-id="d0e8e-108">DESCRIPTION</span></span>
<span data-ttu-id="d0e8e-109">更新 IoT 中央應用程式的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="d0e8e-109">Update the metadata for an IoT Central Application.</span></span> 

## <span data-ttu-id="d0e8e-110">示例</span><span class="sxs-lookup"><span data-stu-id="d0e8e-110">EXAMPLES</span></span>

### <span data-ttu-id="d0e8e-111">範例1更新顯示名稱</span><span class="sxs-lookup"><span data-stu-id="d0e8e-111">Example 1 Update Display Name</span></span>
```powershell
PS C:\> Set-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -DisplayName "My New Custom Display Name"
```

<span data-ttu-id="d0e8e-112">更新現有 IoT 中央應用程式的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="d0e8e-112">Update the Display name on an existing IoT Central Application.</span></span>

<span data-ttu-id="d0e8e-113">範例輸出：</span><span class="sxs-lookup"><span data-stu-id="d0e8e-113">Example Output:</span></span>

<span data-ttu-id="d0e8e-114">ResourceId：/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft。IoTCentral/IoTApps/MyAppResourceName 名稱： MyAppResourceName 類型：/IoTCentral 位置： IoTApps 標記： Sku：：的。 westus ApplicationId： [XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX]-xxxx xxxx：我的新自訂顯示名稱子域： IoTCentral 範本： iotc-default@1.0.0 SubscriptionId： xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx-Xxxx PSIotCentralAppSkuInfo： MyAppSubdomain</span><span class="sxs-lookup"><span data-stu-id="d0e8e-114">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My New Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

## <span data-ttu-id="d0e8e-115">參數</span><span class="sxs-lookup"><span data-stu-id="d0e8e-115">PARAMETERS</span></span>

### <span data-ttu-id="d0e8e-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d0e8e-116">-AsJob</span></span>
<span data-ttu-id="d0e8e-117">在背景中執行 Cmdlet 作為作業。</span><span class="sxs-lookup"><span data-stu-id="d0e8e-117">Run cmdlet as a job in the background.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0e8e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0e8e-118">-DefaultProfile</span></span>
<span data-ttu-id="d0e8e-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d0e8e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0e8e-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="d0e8e-120">-DisplayName</span></span>
<span data-ttu-id="d0e8e-121">Iot 中央應用程式的自訂顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="d0e8e-121">Custom Display Name of the Iot Central Application.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0e8e-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d0e8e-122">-InputObject</span></span>
<span data-ttu-id="d0e8e-123">Iot 中央應用程式輸入物件。</span><span class="sxs-lookup"><span data-stu-id="d0e8e-123">Iot Central Application Input Object.</span></span>

```yaml
Type: PSIotCentralApp
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d0e8e-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="d0e8e-124">-Name</span></span>
<span data-ttu-id="d0e8e-125">Iot 中心應用程式資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="d0e8e-125">Name of the Iot Central Application Resource.</span></span>

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

### <span data-ttu-id="d0e8e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0e8e-126">-ResourceGroupName</span></span>
<span data-ttu-id="d0e8e-127">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d0e8e-127">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="d0e8e-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d0e8e-128">-ResourceId</span></span>
<span data-ttu-id="d0e8e-129">Iot 中心應用程式資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="d0e8e-129">Iot Central Application Resource Id.</span></span>

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

### <span data-ttu-id="d0e8e-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="d0e8e-130">-Tag</span></span>
<span data-ttu-id="d0e8e-131">Iot 中心應用程式資源標記。</span><span class="sxs-lookup"><span data-stu-id="d0e8e-131">Iot Central Application Resource Tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0e8e-132">-確認</span><span class="sxs-lookup"><span data-stu-id="d0e8e-132">-Confirm</span></span>
<span data-ttu-id="d0e8e-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d0e8e-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0e8e-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0e8e-134">-WhatIf</span></span>
<span data-ttu-id="d0e8e-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d0e8e-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0e8e-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d0e8e-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0e8e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0e8e-137">CommonParameters</span></span>
<span data-ttu-id="d0e8e-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d0e8e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0e8e-139">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d0e8e-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0e8e-140">輸入</span><span class="sxs-lookup"><span data-stu-id="d0e8e-140">INPUTS</span></span>

### <span data-ttu-id="d0e8e-141">System.object</span><span class="sxs-lookup"><span data-stu-id="d0e8e-141">System.String</span></span>
### <span data-ttu-id="d0e8e-142">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="d0e8e-142">System.Collections.Hashtable</span></span>
### <span data-ttu-id="d0e8e-143">PSIotCentralApp 中的 IotCentral。</span><span class="sxs-lookup"><span data-stu-id="d0e8e-143">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>
## <span data-ttu-id="d0e8e-144">輸出</span><span class="sxs-lookup"><span data-stu-id="d0e8e-144">OUTPUTS</span></span>

### <span data-ttu-id="d0e8e-145">PSIotCentralApp 中的 IotCentral。</span><span class="sxs-lookup"><span data-stu-id="d0e8e-145">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>
## <span data-ttu-id="d0e8e-146">筆記</span><span class="sxs-lookup"><span data-stu-id="d0e8e-146">NOTES</span></span>

## <span data-ttu-id="d0e8e-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="d0e8e-147">RELATED LINKS</span></span>
