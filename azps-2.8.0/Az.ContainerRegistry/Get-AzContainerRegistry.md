---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistry.md
ms.openlocfilehash: f833d2f46c67964356f48a06c35d41dfcf090fdb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613077"
---
# <span data-ttu-id="aecd0-101">Get-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="aecd0-101">Get-AzContainerRegistry</span></span>

## <span data-ttu-id="aecd0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="aecd0-102">SYNOPSIS</span></span>
<span data-ttu-id="aecd0-103">取得容器註冊。</span><span class="sxs-lookup"><span data-stu-id="aecd0-103">Gets a container registry.</span></span>

## <span data-ttu-id="aecd0-104">句法</span><span class="sxs-lookup"><span data-stu-id="aecd0-104">SYNTAX</span></span>

### <span data-ttu-id="aecd0-105">ListRegistriesParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="aecd0-105">ListRegistriesParameterSet (Default)</span></span>
```
Get-AzContainerRegistry [[-ResourceGroupName] <String>] [-IncludeDetail]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aecd0-106">RegistryNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="aecd0-106">RegistryNameParameterSet</span></span>
```
Get-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-IncludeDetail]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aecd0-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="aecd0-107">ResourceIdParameterSet</span></span>
```
Get-AzContainerRegistry [-IncludeDetail] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="aecd0-108">說明</span><span class="sxs-lookup"><span data-stu-id="aecd0-108">DESCRIPTION</span></span>
<span data-ttu-id="aecd0-109">Get-AzContainerRegistry Cmdlet 會取得指定的容器登錄，或資源群組或訂閱中的所有容器註冊機構。</span><span class="sxs-lookup"><span data-stu-id="aecd0-109">The Get-AzContainerRegistry cmdlet gets a specified container registry or all the container registries in a resource group or the subscription.</span></span>

## <span data-ttu-id="aecd0-110">示例</span><span class="sxs-lookup"><span data-stu-id="aecd0-110">EXAMPLES</span></span>

### <span data-ttu-id="aecd0-111">範例1：取得指定的樹枝 registry</span><span class="sxs-lookup"><span data-stu-id="aecd0-111">Example 1: Get a specified container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"

   Container registry location: westus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="aecd0-112">這個命令會取得指定的容器註冊。</span><span class="sxs-lookup"><span data-stu-id="aecd0-112">This command gets the specified container registry.</span></span>

### <span data-ttu-id="aecd0-113">範例2：取得資源群組中的所有容器註冊表</span><span class="sxs-lookup"><span data-stu-id="aecd0-113">Example 2: Get all the container registries in a resource group</span></span>
```powershell
PS C:\>Get-AzContainerRegistry -ResourceGroupName "MyResourceGroup"

   Container registry location: westus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True


   Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry1       Premium    myregistry1.azurecr.io    10/31/2017 6:29:31 PM      Succeeded  True
```

<span data-ttu-id="aecd0-114">這個命令會取得資源群組中的所有容器註冊表。</span><span class="sxs-lookup"><span data-stu-id="aecd0-114">This command gets all the container registries in a resource group.</span></span>

### <span data-ttu-id="aecd0-115">範例3：取得訂閱中的所有容器註冊表</span><span class="sxs-lookup"><span data-stu-id="aecd0-115">Example 3:  Get all the container registries in the subscription</span></span>
```powershell
PS C:\>Get-AzContainerRegistry

  Container registry location: westus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True


   Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry1       Premium    myregistry1.azurecr.io    10/31/2017 6:29:31 PM      Succeeded  True
```

<span data-ttu-id="aecd0-116">這個命令會取得訂閱中的所有容器註冊表。</span><span class="sxs-lookup"><span data-stu-id="aecd0-116">This command gets all the container registries in the subscription.</span></span>

## <span data-ttu-id="aecd0-117">參數</span><span class="sxs-lookup"><span data-stu-id="aecd0-117">PARAMETERS</span></span>

### <span data-ttu-id="aecd0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aecd0-118">-DefaultProfile</span></span>
<span data-ttu-id="aecd0-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="aecd0-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aecd0-120">-IncludeDetail</span><span class="sxs-lookup"><span data-stu-id="aecd0-120">-IncludeDetail</span></span>
<span data-ttu-id="aecd0-121">顯示更多關於容器註冊表的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="aecd0-121">Show more details about the container registry.</span></span>

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

### <span data-ttu-id="aecd0-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="aecd0-122">-Name</span></span>
<span data-ttu-id="aecd0-123">容器登錄名。</span><span class="sxs-lookup"><span data-stu-id="aecd0-123">Container Registry Name.</span></span>

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

### <span data-ttu-id="aecd0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aecd0-124">-ResourceGroupName</span></span>
<span data-ttu-id="aecd0-125">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="aecd0-125">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListRegistriesParameterSet
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

### <span data-ttu-id="aecd0-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aecd0-126">-ResourceId</span></span>
<span data-ttu-id="aecd0-127">容器登錄資源識別碼</span><span class="sxs-lookup"><span data-stu-id="aecd0-127">The container registry resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aecd0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aecd0-128">CommonParameters</span></span>
<span data-ttu-id="aecd0-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="aecd0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aecd0-130">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="aecd0-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aecd0-131">輸入</span><span class="sxs-lookup"><span data-stu-id="aecd0-131">INPUTS</span></span>

### <span data-ttu-id="aecd0-132">System.object</span><span class="sxs-lookup"><span data-stu-id="aecd0-132">System.String</span></span>

## <span data-ttu-id="aecd0-133">輸出</span><span class="sxs-lookup"><span data-stu-id="aecd0-133">OUTPUTS</span></span>

### <span data-ttu-id="aecd0-134">PSContainerRegistry 中的 ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="aecd0-134">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="aecd0-135">筆記</span><span class="sxs-lookup"><span data-stu-id="aecd0-135">NOTES</span></span>

## <span data-ttu-id="aecd0-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="aecd0-136">RELATED LINKS</span></span>

[<span data-ttu-id="aecd0-137">新-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="aecd0-137">New-AzContainerRegistry</span></span>](New-AzContainerRegistry.md)

[<span data-ttu-id="aecd0-138">更新-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="aecd0-138">Update-AzContainerRegistry</span></span>](Update-AzContainerRegistry.md)

[<span data-ttu-id="aecd0-139">移除-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="aecd0-139">Remove-AzContainerRegistry</span></span>](Remove-AzContainerRegistry.md)
