---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistry.md
ms.openlocfilehash: ce2cabd669f779fe94afa80089868aa04753524b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450827"
---
# <span data-ttu-id="15d14-101">Get-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="15d14-101">Get-AzureRmContainerRegistry</span></span>

## <span data-ttu-id="15d14-102">摘要</span><span class="sxs-lookup"><span data-stu-id="15d14-102">SYNOPSIS</span></span>
<span data-ttu-id="15d14-103">取得容器註冊。</span><span class="sxs-lookup"><span data-stu-id="15d14-103">Gets a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="15d14-104">句法</span><span class="sxs-lookup"><span data-stu-id="15d14-104">SYNTAX</span></span>

### <span data-ttu-id="15d14-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="15d14-105">ResourceGroupParameterSet</span></span>
```
Get-AzureRmContainerRegistry [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="15d14-106">RegistryNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="15d14-106">RegistryNameParameterSet</span></span>
```
Get-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="15d14-107">說明</span><span class="sxs-lookup"><span data-stu-id="15d14-107">DESCRIPTION</span></span>
<span data-ttu-id="15d14-108">**AzureRmContainerRegistry** Cmdlet 會取得指定的容器登錄，或資源群組或訂閱中的所有容器註冊表。</span><span class="sxs-lookup"><span data-stu-id="15d14-108">The **Get-AzureRmContainerRegistry** cmdlet gets a specified container registry or all the container registries in a resource group or the subscription.</span></span>

## <span data-ttu-id="15d14-109">示例</span><span class="sxs-lookup"><span data-stu-id="15d14-109">EXAMPLES</span></span>

### <span data-ttu-id="15d14-110">範例1：取得指定的樹枝 registry</span><span class="sxs-lookup"><span data-stu-id="15d14-110">Example 1: Get a specified container registry</span></span>
```
PS C:\>Get-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"

Id                 : /subscriptions/3eb31d8d-2879-4706-89b4-4dc4047726c6/resourceGroups/MyResourceGroup/providers/Microsoft.ContainerRegistry/registries/MyRegistry
ResourceGroupName  : MyResourceGroup
Name               : MyRegistry
Type               : Microsoft.ContainerRegistry/registries
Location           : westus
Tags               : {}
SkuName            : Basic
SkuTier            : Basic
LoginServer        : myregistry.azurecr.io
CreationDate       : 4/13/2017 3:48:57 PM
ProvisioningState  : Succeeded
AdminUserEnabled   : False
StorageAccountName : myregistry154817
```

<span data-ttu-id="15d14-111">這個命令會取得指定的容器註冊。</span><span class="sxs-lookup"><span data-stu-id="15d14-111">This command gets the specified container registry.</span></span>

### <span data-ttu-id="15d14-112">範例2：取得資源群組中的所有容器註冊表</span><span class="sxs-lookup"><span data-stu-id="15d14-112">Example 2: Get all the container registries in a resource group</span></span>
```
PS C:\>Get-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup"

Id                 : /subscriptions/3eb31d8d-2879-4706-89b4-4dc4047726c6/resourceGroups/MyResourceGroup/providers/Microsoft.ContainerRegistry/registries/MyRegistry
ResourceGroupName  : MyResourceGroup
Name               : MyRegistry
Type               : Microsoft.ContainerRegistry/registries
Location           : westus
Tags               : {}
SkuName            : Basic
SkuTier            : Basic
LoginServer        : myregistry.azurecr.io
CreationDate       : 4/13/2017 3:48:57 PM
ProvisioningState  : Succeeded
AdminUserEnabled   : False
StorageAccountName : myregistry154817

Id                 : /subscriptions/3eb31d8d-2879-4706-89b4-4dc4047726c6/resourceGroups/MyResourceGroup/providers/Microsoft.ContainerRegistry/registries/AnotherRegistry
ResourceGroupName  : MyResourceGroup
Name               : AnotherRegistry
Type               : Microsoft.ContainerRegistry/registries
Location           : westus
Tags               : {}
SkuName            : Basic
SkuTier            : Basic
LoginServer        : anotherregistry.azurecr.io
CreationDate       : 4/13/2017 3:50:49 PM
ProvisioningState  : Succeeded
AdminUserEnabled   : True
StorageAccountName : anotherregistry154940
```

<span data-ttu-id="15d14-113">這個命令會取得資源群組中的所有容器註冊表。</span><span class="sxs-lookup"><span data-stu-id="15d14-113">This command gets all the container registries in a resource group.</span></span>

### <span data-ttu-id="15d14-114">範例3：取得訂閱中的所有容器註冊表</span><span class="sxs-lookup"><span data-stu-id="15d14-114">Example 3:  Get all the container registries in the subscription</span></span>
```
PS C:\>Get-AzureRmContainerRegistry

Id                 : /subscriptions/3eb31d8d-2879-4706-89b4-4dc4047726c6/resourceGroups/MyResourceGroup/providers/Microsoft.ContainerRegistry/registries/MyRegistry
ResourceGroupName  : MyResourceGroup
Name               : MyRegistry
Type               : Microsoft.ContainerRegistry/registries
Location           : westus
Tags               : {}
SkuName            : Basic
SkuTier            : Basic
LoginServer        : myregistry.azurecr.io
CreationDate       : 4/13/2017 3:48:57 PM
ProvisioningState  : Succeeded
AdminUserEnabled   : False
StorageAccountName : myregistry154817

Id                 : /subscriptions/3eb31d8d-2879-4706-89b4-4dc4047726c6/resourceGroups/MyResourceGroup/providers/Microsoft.ContainerRegistry/registries/AnotherRegistry
ResourceGroupName  : MyResourceGroup
Name               : AnotherRegistry
Type               : Microsoft.ContainerRegistry/registries
Location           : westus
Tags               : {}
SkuName            : Basic
SkuTier            : Basic
LoginServer        : anotherregistry.azurecr.io
CreationDate       : 4/13/2017 3:50:49 PM
ProvisioningState  : Succeeded
AdminUserEnabled   : True
StorageAccountName : anotherregistry154940
```

<span data-ttu-id="15d14-115">這個命令會取得訂閱中的所有容器註冊表。</span><span class="sxs-lookup"><span data-stu-id="15d14-115">This command gets all the container registries in the subscription.</span></span>

## <span data-ttu-id="15d14-116">參數</span><span class="sxs-lookup"><span data-stu-id="15d14-116">PARAMETERS</span></span>

### <span data-ttu-id="15d14-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="15d14-117">-Name</span></span>
<span data-ttu-id="15d14-118">容器登錄名。</span><span class="sxs-lookup"><span data-stu-id="15d14-118">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: RegistryNameParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15d14-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15d14-119">-ResourceGroupName</span></span>
<span data-ttu-id="15d14-120">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="15d14-120">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: RegistryNameParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15d14-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15d14-121">-DefaultProfile</span></span>
<span data-ttu-id="15d14-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="15d14-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="15d14-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15d14-123">CommonParameters</span></span>
<span data-ttu-id="15d14-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="15d14-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15d14-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="15d14-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15d14-126">輸入</span><span class="sxs-lookup"><span data-stu-id="15d14-126">INPUTS</span></span>

## <span data-ttu-id="15d14-127">輸出</span><span class="sxs-lookup"><span data-stu-id="15d14-127">OUTPUTS</span></span>

### <span data-ttu-id="15d14-128">PSContainerRegistry 中的 ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="15d14-128">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="15d14-129">筆記</span><span class="sxs-lookup"><span data-stu-id="15d14-129">NOTES</span></span>

## <span data-ttu-id="15d14-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="15d14-130">RELATED LINKS</span></span>

[<span data-ttu-id="15d14-131">新-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="15d14-131">New-AzureRmContainerRegistry</span></span>](./New-AzureRmContainerRegistry.md)

[<span data-ttu-id="15d14-132">更新-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="15d14-132">Update-AzureRmContainerRegistry</span></span>](./Update-AzureRmContainerRegistry.md)

[<span data-ttu-id="15d14-133">移除-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="15d14-133">Remove-AzureRmContainerRegistry</span></span>](./Remove-AzureRmContainerRegistry.md)

