---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/set-aziothubedgemodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubEdgeModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubEdgeModule.md
ms.openlocfilehash: f3bc819c7050300c82f039981b1df34010771eb7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902078"
---
# <span data-ttu-id="4a80b-101">Set-AzIotHubEdgeModule</span><span class="sxs-lookup"><span data-stu-id="4a80b-101">Set-AzIotHubEdgeModule</span></span>

## <span data-ttu-id="4a80b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="4a80b-102">SYNOPSIS</span></span>
<span data-ttu-id="4a80b-103">在單一邊緣裝置上設定邊緣模組。</span><span class="sxs-lookup"><span data-stu-id="4a80b-103">Set edge modules on a single edge device.</span></span>

## <span data-ttu-id="4a80b-104">語法</span><span class="sxs-lookup"><span data-stu-id="4a80b-104">SYNTAX</span></span>

### <span data-ttu-id="4a80b-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="4a80b-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubEdgeModule [-ResourceGroupName] <String> [-IotHubName] <String> -DeviceId <String>
 -ModulesContent <Hashtable> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4a80b-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="4a80b-106">InputObjectSet</span></span>
```
Set-AzIotHubEdgeModule [-InputObject] <PSIotHub> -DeviceId <String> -ModulesContent <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a80b-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="4a80b-107">ResourceIdSet</span></span>
```
Set-AzIotHubEdgeModule [-ResourceId] <String> -DeviceId <String> -ModulesContent <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4a80b-108">描述</span><span class="sxs-lookup"><span data-stu-id="4a80b-108">DESCRIPTION</span></span>
<span data-ttu-id="4a80b-109">將提供的模組組組內容適用于指定的邊緣裝置。</span><span class="sxs-lookup"><span data-stu-id="4a80b-109">Applies the provided modules configuration content to the specified edge device.</span></span>
<span data-ttu-id="4a80b-110">注意：執行時，命令會輸出適用于裝置之模組的集合。</span><span class="sxs-lookup"><span data-stu-id="4a80b-110">Note: Upon execution the command will output the collection of modules applied to the device.</span></span>

## <span data-ttu-id="4a80b-111">例子</span><span class="sxs-lookup"><span data-stu-id="4a80b-111">EXAMPLES</span></span>

### <span data-ttu-id="4a80b-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="4a80b-112">Example 1</span></span>
```powershell
PS C:\> $content = Get-Content "C:/Edge/modules.json" | ConvertFrom-Json -AsHashtable
PS C:\> Set-AzIotHubEdgeModule -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myEdgeDevice1" -ModulesContent $content
```

<span data-ttu-id="4a80b-113">在目標裝置上設定模組以在開發期間測試邊緣模組。</span><span class="sxs-lookup"><span data-stu-id="4a80b-113">Test edge modules while in development by setting modules on a target device.</span></span>

## <span data-ttu-id="4a80b-114">參數</span><span class="sxs-lookup"><span data-stu-id="4a80b-114">PARAMETERS</span></span>

### <span data-ttu-id="4a80b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a80b-115">-DefaultProfile</span></span>
<span data-ttu-id="4a80b-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="4a80b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a80b-117">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="4a80b-117">-DeviceId</span></span>
<span data-ttu-id="4a80b-118">Target Edge 裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="4a80b-118">Target Edge Device Id.</span></span>

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

### <span data-ttu-id="4a80b-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4a80b-119">-InputObject</span></span>
<span data-ttu-id="4a80b-120">IotHub 物件</span><span class="sxs-lookup"><span data-stu-id="4a80b-120">IotHub object</span></span>

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

### <span data-ttu-id="4a80b-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="4a80b-121">-IotHubName</span></span>
<span data-ttu-id="4a80b-122">Iot Hub 的名稱</span><span class="sxs-lookup"><span data-stu-id="4a80b-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="4a80b-123">-ModulesContent</span><span class="sxs-lookup"><span data-stu-id="4a80b-123">-ModulesContent</span></span>
<span data-ttu-id="4a80b-124">IoT Edge 裝置模組的組組內容。</span><span class="sxs-lookup"><span data-stu-id="4a80b-124">Configuration content of modules for IoT Edge devices.</span></span>

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

### <span data-ttu-id="4a80b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a80b-125">-ResourceGroupName</span></span>
<span data-ttu-id="4a80b-126">資源組的名稱</span><span class="sxs-lookup"><span data-stu-id="4a80b-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="4a80b-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4a80b-127">-ResourceId</span></span>
<span data-ttu-id="4a80b-128">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="4a80b-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="4a80b-129">-確認</span><span class="sxs-lookup"><span data-stu-id="4a80b-129">-Confirm</span></span>
<span data-ttu-id="4a80b-130">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="4a80b-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a80b-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a80b-131">-WhatIf</span></span>
<span data-ttu-id="4a80b-132">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4a80b-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4a80b-133">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4a80b-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a80b-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a80b-134">CommonParameters</span></span>
<span data-ttu-id="4a80b-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="4a80b-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a80b-136">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="4a80b-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a80b-137">輸入</span><span class="sxs-lookup"><span data-stu-id="4a80b-137">INPUTS</span></span>

### <span data-ttu-id="4a80b-138">Microsoft.Azure.Commands.management.IotHub.models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="4a80b-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="4a80b-139">System.String</span><span class="sxs-lookup"><span data-stu-id="4a80b-139">System.String</span></span>

## <span data-ttu-id="4a80b-140">輸出</span><span class="sxs-lookup"><span data-stu-id="4a80b-140">OUTPUTS</span></span>

### <span data-ttu-id="4a80b-141">Microsoft.Azure.Commands.management.IotHub.models.PSModules[]</span><span class="sxs-lookup"><span data-stu-id="4a80b-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSModules[]</span></span>

## <span data-ttu-id="4a80b-142">筆記</span><span class="sxs-lookup"><span data-stu-id="4a80b-142">NOTES</span></span>

## <span data-ttu-id="4a80b-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="4a80b-143">RELATED LINKS</span></span>
