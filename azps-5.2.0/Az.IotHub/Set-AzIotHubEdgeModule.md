---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubedgemodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubEdgeModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubEdgeModule.md
ms.openlocfilehash: 5316b6bae6bfc64f791959bb6e236c861833ed4c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98281017"
---
# <span data-ttu-id="a6f1a-101">Set-AzIotHubEdgeModule</span><span class="sxs-lookup"><span data-stu-id="a6f1a-101">Set-AzIotHubEdgeModule</span></span>

## <span data-ttu-id="a6f1a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a6f1a-102">SYNOPSIS</span></span>
<span data-ttu-id="a6f1a-103">在單一邊緣裝置上設定邊緣模組。</span><span class="sxs-lookup"><span data-stu-id="a6f1a-103">Set edge modules on a single edge device.</span></span>

## <span data-ttu-id="a6f1a-104">句法</span><span class="sxs-lookup"><span data-stu-id="a6f1a-104">SYNTAX</span></span>

### <span data-ttu-id="a6f1a-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="a6f1a-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubEdgeModule [-ResourceGroupName] <String> [-IotHubName] <String> -DeviceId <String>
 -ModulesContent <Hashtable> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a6f1a-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a6f1a-106">InputObjectSet</span></span>
```
Set-AzIotHubEdgeModule [-InputObject] <PSIotHub> -DeviceId <String> -ModulesContent <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6f1a-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="a6f1a-107">ResourceIdSet</span></span>
```
Set-AzIotHubEdgeModule [-ResourceId] <String> -DeviceId <String> -ModulesContent <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6f1a-108">說明</span><span class="sxs-lookup"><span data-stu-id="a6f1a-108">DESCRIPTION</span></span>
<span data-ttu-id="a6f1a-109">將提供的模組配置內容套用到指定的邊緣裝置。</span><span class="sxs-lookup"><span data-stu-id="a6f1a-109">Applies the provided modules configuration content to the specified edge device.</span></span>
<span data-ttu-id="a6f1a-110">注意：執行時，命令會輸出套用到裝置的模組集合。</span><span class="sxs-lookup"><span data-stu-id="a6f1a-110">Note: Upon execution the command will output the collection of modules applied to the device.</span></span>

## <span data-ttu-id="a6f1a-111">示例</span><span class="sxs-lookup"><span data-stu-id="a6f1a-111">EXAMPLES</span></span>

### <span data-ttu-id="a6f1a-112">範例1</span><span class="sxs-lookup"><span data-stu-id="a6f1a-112">Example 1</span></span>
```powershell
PS C:\> $content = Get-Content "C:/Edge/modules.json" | ConvertFrom-Json -AsHashtable
PS C:\> Set-AzIotHubEdgeModule -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myEdgeDevice1" -ModulesContent $content
```

<span data-ttu-id="a6f1a-113">在開發期間，在目標裝置上設定模組，以測試 edge 模組。</span><span class="sxs-lookup"><span data-stu-id="a6f1a-113">Test edge modules while in development by setting modules on a target device.</span></span>

## <span data-ttu-id="a6f1a-114">參數</span><span class="sxs-lookup"><span data-stu-id="a6f1a-114">PARAMETERS</span></span>

### <span data-ttu-id="a6f1a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6f1a-115">-DefaultProfile</span></span>
<span data-ttu-id="a6f1a-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a6f1a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6f1a-117">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="a6f1a-117">-DeviceId</span></span>
<span data-ttu-id="a6f1a-118">目標邊緣裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="a6f1a-118">Target Edge Device Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6f1a-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a6f1a-119">-InputObject</span></span>
<span data-ttu-id="a6f1a-120">IotHub 物件</span><span class="sxs-lookup"><span data-stu-id="a6f1a-120">IotHub object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a6f1a-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="a6f1a-121">-IotHubName</span></span>
<span data-ttu-id="a6f1a-122">Iot 中樞的名稱</span><span class="sxs-lookup"><span data-stu-id="a6f1a-122">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6f1a-123">-ModulesContent</span><span class="sxs-lookup"><span data-stu-id="a6f1a-123">-ModulesContent</span></span>
<span data-ttu-id="a6f1a-124">IoT Edge 裝置的模組配置內容。</span><span class="sxs-lookup"><span data-stu-id="a6f1a-124">Configuration content of modules for IoT Edge devices.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6f1a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6f1a-125">-ResourceGroupName</span></span>
<span data-ttu-id="a6f1a-126">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="a6f1a-126">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6f1a-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a6f1a-127">-ResourceId</span></span>
<span data-ttu-id="a6f1a-128">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="a6f1a-128">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6f1a-129">-確認</span><span class="sxs-lookup"><span data-stu-id="a6f1a-129">-Confirm</span></span>
<span data-ttu-id="a6f1a-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a6f1a-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6f1a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6f1a-131">-WhatIf</span></span>
<span data-ttu-id="a6f1a-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a6f1a-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6f1a-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a6f1a-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6f1a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6f1a-134">CommonParameters</span></span>
<span data-ttu-id="a6f1a-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a6f1a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6f1a-136">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a6f1a-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6f1a-137">輸入</span><span class="sxs-lookup"><span data-stu-id="a6f1a-137">INPUTS</span></span>

### <span data-ttu-id="a6f1a-138">PSIotHub （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="a6f1a-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="a6f1a-139">System.object</span><span class="sxs-lookup"><span data-stu-id="a6f1a-139">System.String</span></span>

## <span data-ttu-id="a6f1a-140">輸出</span><span class="sxs-lookup"><span data-stu-id="a6f1a-140">OUTPUTS</span></span>

### <span data-ttu-id="a6f1a-141">PSModules []. IotHub. []</span><span class="sxs-lookup"><span data-stu-id="a6f1a-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSModules[]</span></span>

## <span data-ttu-id="a6f1a-142">筆記</span><span class="sxs-lookup"><span data-stu-id="a6f1a-142">NOTES</span></span>

## <span data-ttu-id="a6f1a-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="a6f1a-143">RELATED LINKS</span></span>
