---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/remove-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistry.md
ms.openlocfilehash: df0c938db8f44ebffedc9760e4a3d33ee175ae01
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449912"
---
# <span data-ttu-id="87d8f-101">Remove-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="87d8f-101">Remove-AzureRmContainerRegistry</span></span>

## <span data-ttu-id="87d8f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="87d8f-102">SYNOPSIS</span></span>
<span data-ttu-id="87d8f-103">移除容器註冊。</span><span class="sxs-lookup"><span data-stu-id="87d8f-103">Removes a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="87d8f-104">句法</span><span class="sxs-lookup"><span data-stu-id="87d8f-104">SYNTAX</span></span>

### <span data-ttu-id="87d8f-105">NameResourceGroupParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="87d8f-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87d8f-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="87d8f-106">RegistryObjectParameterSet</span></span>
```
Remove-AzureRmContainerRegistry -Registry <PSContainerRegistry> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87d8f-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="87d8f-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmContainerRegistry -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="87d8f-108">說明</span><span class="sxs-lookup"><span data-stu-id="87d8f-108">DESCRIPTION</span></span>
<span data-ttu-id="87d8f-109">Remove-AzureRmContainerRegistry Cmdlet 會移除容器註冊。</span><span class="sxs-lookup"><span data-stu-id="87d8f-109">The Remove-AzureRmContainerRegistry cmdlet removes a container registry.</span></span>

## <span data-ttu-id="87d8f-110">示例</span><span class="sxs-lookup"><span data-stu-id="87d8f-110">EXAMPLES</span></span>

### <span data-ttu-id="87d8f-111">範例1：移除指定的容器註冊表</span><span class="sxs-lookup"><span data-stu-id="87d8f-111">Example 1: Remove a specified container registry</span></span>
```powershell
PS C:\>Remove-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"
```

<span data-ttu-id="87d8f-112">這個命令會移除指定的容器註冊。</span><span class="sxs-lookup"><span data-stu-id="87d8f-112">This command removes the specified container registry.</span></span>

## <span data-ttu-id="87d8f-113">參數</span><span class="sxs-lookup"><span data-stu-id="87d8f-113">PARAMETERS</span></span>

### <span data-ttu-id="87d8f-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="87d8f-114">-Name</span></span>
<span data-ttu-id="87d8f-115">容器登錄名。</span><span class="sxs-lookup"><span data-stu-id="87d8f-115">Container Registry Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87d8f-116">-Registry</span><span class="sxs-lookup"><span data-stu-id="87d8f-116">-Registry</span></span>
<span data-ttu-id="87d8f-117">分枝 Registry 物件。</span><span class="sxs-lookup"><span data-stu-id="87d8f-117">Container Registry Object.</span></span>

```yaml
Type: PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87d8f-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87d8f-118">-ResourceGroupName</span></span>
<span data-ttu-id="87d8f-119">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="87d8f-119">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87d8f-120">-確認</span><span class="sxs-lookup"><span data-stu-id="87d8f-120">-Confirm</span></span>
<span data-ttu-id="87d8f-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="87d8f-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87d8f-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87d8f-122">-WhatIf</span></span>
<span data-ttu-id="87d8f-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="87d8f-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87d8f-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="87d8f-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87d8f-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87d8f-125">-DefaultProfile</span></span>
<span data-ttu-id="87d8f-126">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="87d8f-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="87d8f-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="87d8f-127">-ResourceId</span></span>
<span data-ttu-id="87d8f-128">容器登錄資源識別碼</span><span class="sxs-lookup"><span data-stu-id="87d8f-128">The container registry resource id</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87d8f-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="87d8f-129">-PassThru</span></span>
<span data-ttu-id="87d8f-130">表示如果移除成功，此 Cmdlet 會傳回 true。</span><span class="sxs-lookup"><span data-stu-id="87d8f-130">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="87d8f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87d8f-131">CommonParameters</span></span>
<span data-ttu-id="87d8f-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="87d8f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87d8f-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="87d8f-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87d8f-134">輸入</span><span class="sxs-lookup"><span data-stu-id="87d8f-134">INPUTS</span></span>

### <span data-ttu-id="87d8f-135">PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="87d8f-135">PSContainerRegistry</span></span>
<span data-ttu-id="87d8f-136">參數 "Registry" 接受管線中 "PSContainerRegistry" 類型的值</span><span class="sxs-lookup"><span data-stu-id="87d8f-136">Parameter 'Registry' accepts value of type 'PSContainerRegistry' from the pipeline</span></span>

## <span data-ttu-id="87d8f-137">輸出</span><span class="sxs-lookup"><span data-stu-id="87d8f-137">OUTPUTS</span></span>

### <span data-ttu-id="87d8f-138">所有</span><span class="sxs-lookup"><span data-stu-id="87d8f-138">None</span></span>

## <span data-ttu-id="87d8f-139">筆記</span><span class="sxs-lookup"><span data-stu-id="87d8f-139">NOTES</span></span>

## <span data-ttu-id="87d8f-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="87d8f-140">RELATED LINKS</span></span>

[<span data-ttu-id="87d8f-141">新-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="87d8f-141">New-AzureRmContainerRegistry</span></span>]()

[<span data-ttu-id="87d8f-142">AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="87d8f-142">Get-AzureRmContainerRegistry</span></span>]()

[<span data-ttu-id="87d8f-143">更新-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="87d8f-143">Update-AzureRmContainerRegistry</span></span>]()

