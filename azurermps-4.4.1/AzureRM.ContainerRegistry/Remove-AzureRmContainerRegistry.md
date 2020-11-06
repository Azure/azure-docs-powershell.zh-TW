---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistry.md
ms.openlocfilehash: 5a5ea87044c18e82f4c17294356a35adb254eee4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446876"
---
# <span data-ttu-id="dc59f-101">Remove-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="dc59f-101">Remove-AzureRmContainerRegistry</span></span>

## <span data-ttu-id="dc59f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="dc59f-102">SYNOPSIS</span></span>
<span data-ttu-id="dc59f-103">移除容器註冊。</span><span class="sxs-lookup"><span data-stu-id="dc59f-103">Removes a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dc59f-104">句法</span><span class="sxs-lookup"><span data-stu-id="dc59f-104">SYNTAX</span></span>

### <span data-ttu-id="dc59f-105">NameResourceGroupParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="dc59f-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc59f-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc59f-106">RegistryObjectParameterSet</span></span>
```
Remove-AzureRmContainerRegistry -Registry <PSContainerRegistry> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dc59f-107">說明</span><span class="sxs-lookup"><span data-stu-id="dc59f-107">DESCRIPTION</span></span>
<span data-ttu-id="dc59f-108">**AzureRmContainerRegistry** Cmdlet 會移除容器註冊。</span><span class="sxs-lookup"><span data-stu-id="dc59f-108">The **Remove-AzureRmContainerRegistry** cmdlet removes a container registry.</span></span>

## <span data-ttu-id="dc59f-109">示例</span><span class="sxs-lookup"><span data-stu-id="dc59f-109">EXAMPLES</span></span>

### <span data-ttu-id="dc59f-110">範例1：移除指定的容器註冊表</span><span class="sxs-lookup"><span data-stu-id="dc59f-110">Example 1: Remove a specified container registry</span></span>
```
PS C:\>Remove-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"
```

<span data-ttu-id="dc59f-111">這個命令會移除指定的容器註冊。</span><span class="sxs-lookup"><span data-stu-id="dc59f-111">This command removes the specified container registry.</span></span>

## <span data-ttu-id="dc59f-112">參數</span><span class="sxs-lookup"><span data-stu-id="dc59f-112">PARAMETERS</span></span>

### <span data-ttu-id="dc59f-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="dc59f-113">-Name</span></span>
<span data-ttu-id="dc59f-114">容器登錄名。</span><span class="sxs-lookup"><span data-stu-id="dc59f-114">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc59f-115">-Registry</span><span class="sxs-lookup"><span data-stu-id="dc59f-115">-Registry</span></span>
<span data-ttu-id="dc59f-116">分枝 Registry 物件。</span><span class="sxs-lookup"><span data-stu-id="dc59f-116">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dc59f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc59f-117">-ResourceGroupName</span></span>
<span data-ttu-id="dc59f-118">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="dc59f-118">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc59f-119">-確認</span><span class="sxs-lookup"><span data-stu-id="dc59f-119">-Confirm</span></span>
<span data-ttu-id="dc59f-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="dc59f-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc59f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc59f-121">-WhatIf</span></span>
<span data-ttu-id="dc59f-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="dc59f-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc59f-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="dc59f-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc59f-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc59f-124">-DefaultProfile</span></span>
<span data-ttu-id="dc59f-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="dc59f-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc59f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc59f-126">CommonParameters</span></span>
<span data-ttu-id="dc59f-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="dc59f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc59f-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="dc59f-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc59f-129">輸入</span><span class="sxs-lookup"><span data-stu-id="dc59f-129">INPUTS</span></span>

### <span data-ttu-id="dc59f-130">PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="dc59f-130">PSContainerRegistry</span></span>
<span data-ttu-id="dc59f-131">參數 "Registry" 接受管線中 "PSContainerRegistry" 類型的值</span><span class="sxs-lookup"><span data-stu-id="dc59f-131">Parameter 'Registry' accepts value of type 'PSContainerRegistry' from the pipeline</span></span>

## <span data-ttu-id="dc59f-132">輸出</span><span class="sxs-lookup"><span data-stu-id="dc59f-132">OUTPUTS</span></span>

### <span data-ttu-id="dc59f-133">所有</span><span class="sxs-lookup"><span data-stu-id="dc59f-133">None</span></span>

## <span data-ttu-id="dc59f-134">筆記</span><span class="sxs-lookup"><span data-stu-id="dc59f-134">NOTES</span></span>

## <span data-ttu-id="dc59f-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="dc59f-135">RELATED LINKS</span></span>

[<span data-ttu-id="dc59f-136">新-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="dc59f-136">New-AzureRmContainerRegistry</span></span>](./New-AzureRmContainerRegistry.md)

[<span data-ttu-id="dc59f-137">AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="dc59f-137">Get-AzureRmContainerRegistry</span></span>](./Get-AzureRmContainerRegistry.md)

[<span data-ttu-id="dc59f-138">更新-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="dc59f-138">Update-AzureRmContainerRegistry</span></span>](./Update-AzureRmContainerRegistry.md)

