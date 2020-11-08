---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubConfiguration.md
ms.openlocfilehash: 0b87bece7bca0ea3f534746dd20a163f69f21262
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93969687"
---
# <span data-ttu-id="c3a17-101">Remove-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="c3a17-101">Remove-AzIotHubConfiguration</span></span>

## <span data-ttu-id="c3a17-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c3a17-102">SYNOPSIS</span></span>
<span data-ttu-id="c3a17-103">刪除 IoT 裝置設定。</span><span class="sxs-lookup"><span data-stu-id="c3a17-103">Delete an IoT device configuration.</span></span>

## <span data-ttu-id="c3a17-104">句法</span><span class="sxs-lookup"><span data-stu-id="c3a17-104">SYNTAX</span></span>

### <span data-ttu-id="c3a17-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="c3a17-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubConfiguration [-ResourceGroupName] <String> [-IotHubName] <String> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3a17-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c3a17-106">InputObjectSet</span></span>
```
Remove-AzIotHubConfiguration [-InputObject] <PSIotHub> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3a17-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="c3a17-107">ResourceIdSet</span></span>
```
Remove-AzIotHubConfiguration [-ResourceId] <String> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3a17-108">說明</span><span class="sxs-lookup"><span data-stu-id="c3a17-108">DESCRIPTION</span></span>
<span data-ttu-id="c3a17-109">如需詳細資訊，請參閱 https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management 。</span><span class="sxs-lookup"><span data-stu-id="c3a17-109">See https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management for more information.</span></span>

## <span data-ttu-id="c3a17-110">示例</span><span class="sxs-lookup"><span data-stu-id="c3a17-110">EXAMPLES</span></span>

### <span data-ttu-id="c3a17-111">範例1</span><span class="sxs-lookup"><span data-stu-id="c3a17-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1"
```

<span data-ttu-id="c3a17-112">刪除 IoT 裝置設定。</span><span class="sxs-lookup"><span data-stu-id="c3a17-112">Delete an IoT device configuration.</span></span>

## <span data-ttu-id="c3a17-113">參數</span><span class="sxs-lookup"><span data-stu-id="c3a17-113">PARAMETERS</span></span>

### <span data-ttu-id="c3a17-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3a17-114">-DefaultProfile</span></span>
<span data-ttu-id="c3a17-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c3a17-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3a17-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c3a17-116">-InputObject</span></span>
<span data-ttu-id="c3a17-117">IotHub 物件</span><span class="sxs-lookup"><span data-stu-id="c3a17-117">IotHub object</span></span>

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

### <span data-ttu-id="c3a17-118">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="c3a17-118">-IotHubName</span></span>
<span data-ttu-id="c3a17-119">Iot 中樞的名稱</span><span class="sxs-lookup"><span data-stu-id="c3a17-119">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="c3a17-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="c3a17-120">-Name</span></span>
<span data-ttu-id="c3a17-121">配置的識別碼。</span><span class="sxs-lookup"><span data-stu-id="c3a17-121">Identifier for the configuration.</span></span>

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

### <span data-ttu-id="c3a17-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c3a17-122">-PassThru</span></span>
<span data-ttu-id="c3a17-123">允許傳回布林值物件。</span><span class="sxs-lookup"><span data-stu-id="c3a17-123">Allows to return the boolean object.</span></span>
<span data-ttu-id="c3a17-124">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="c3a17-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c3a17-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3a17-125">-ResourceGroupName</span></span>
<span data-ttu-id="c3a17-126">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="c3a17-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="c3a17-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c3a17-127">-ResourceId</span></span>
<span data-ttu-id="c3a17-128">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="c3a17-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="c3a17-129">-確認</span><span class="sxs-lookup"><span data-stu-id="c3a17-129">-Confirm</span></span>
<span data-ttu-id="c3a17-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c3a17-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3a17-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3a17-131">-WhatIf</span></span>
<span data-ttu-id="c3a17-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c3a17-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3a17-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c3a17-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3a17-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3a17-134">CommonParameters</span></span>
<span data-ttu-id="c3a17-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c3a17-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3a17-136">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c3a17-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3a17-137">輸入</span><span class="sxs-lookup"><span data-stu-id="c3a17-137">INPUTS</span></span>

### <span data-ttu-id="c3a17-138">PSIotHub （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="c3a17-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="c3a17-139">System.object</span><span class="sxs-lookup"><span data-stu-id="c3a17-139">System.String</span></span>

## <span data-ttu-id="c3a17-140">輸出</span><span class="sxs-lookup"><span data-stu-id="c3a17-140">OUTPUTS</span></span>

### <span data-ttu-id="c3a17-141">System.object</span><span class="sxs-lookup"><span data-stu-id="c3a17-141">System.Boolean</span></span>

## <span data-ttu-id="c3a17-142">筆記</span><span class="sxs-lookup"><span data-stu-id="c3a17-142">NOTES</span></span>

## <span data-ttu-id="c3a17-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="c3a17-143">RELATED LINKS</span></span>
