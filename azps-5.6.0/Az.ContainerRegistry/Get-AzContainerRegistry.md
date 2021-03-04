---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/get-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistry.md
ms.openlocfilehash: 969e37173c487b2ed3ee4ab6dad5374208f5ff27
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915566"
---
# <span data-ttu-id="73519-101">Get-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="73519-101">Get-AzContainerRegistry</span></span>

## <span data-ttu-id="73519-102">簡介</span><span class="sxs-lookup"><span data-stu-id="73519-102">SYNOPSIS</span></span>
<span data-ttu-id="73519-103">獲得容器註冊表。</span><span class="sxs-lookup"><span data-stu-id="73519-103">Gets a container registry.</span></span>

## <span data-ttu-id="73519-104">語法</span><span class="sxs-lookup"><span data-stu-id="73519-104">SYNTAX</span></span>

### <span data-ttu-id="73519-105">ListRegistriesParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="73519-105">ListRegistriesParameterSet (Default)</span></span>
```
Get-AzContainerRegistry [[-ResourceGroupName] <String>] [-IncludeDetail]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="73519-106">RegistryNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="73519-106">RegistryNameParameterSet</span></span>
```
Get-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-IncludeDetail]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="73519-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="73519-107">ResourceIdParameterSet</span></span>
```
Get-AzContainerRegistry [-IncludeDetail] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="73519-108">描述</span><span class="sxs-lookup"><span data-stu-id="73519-108">DESCRIPTION</span></span>
<span data-ttu-id="73519-109">此Get-AzContainerRegistry Cmdlet 會獲得指定的容器註冊表，或資源群組或訂閱中所有的容器註冊表。</span><span class="sxs-lookup"><span data-stu-id="73519-109">The Get-AzContainerRegistry cmdlet gets a specified container registry or all the container registries in a resource group or the subscription.</span></span>

## <span data-ttu-id="73519-110">例子</span><span class="sxs-lookup"><span data-stu-id="73519-110">EXAMPLES</span></span>

### <span data-ttu-id="73519-111">範例 1：取得指定的容器註冊表</span><span class="sxs-lookup"><span data-stu-id="73519-111">Example 1: Get a specified container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"

   Container registry location: westus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="73519-112">此命令會獲得指定的容器註冊表。</span><span class="sxs-lookup"><span data-stu-id="73519-112">This command gets the specified container registry.</span></span>

### <span data-ttu-id="73519-113">範例 2：取得資源群組中所有的容器註冊表</span><span class="sxs-lookup"><span data-stu-id="73519-113">Example 2: Get all the container registries in a resource group</span></span>
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

<span data-ttu-id="73519-114">此命令會獲得資源群組中所有的容器註冊表。</span><span class="sxs-lookup"><span data-stu-id="73519-114">This command gets all the container registries in a resource group.</span></span>

### <span data-ttu-id="73519-115">範例 3：取得訂閱中所有的容器註冊表</span><span class="sxs-lookup"><span data-stu-id="73519-115">Example 3:  Get all the container registries in the subscription</span></span>
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

<span data-ttu-id="73519-116">此命令會獲得訂閱中所有的容器註冊表。</span><span class="sxs-lookup"><span data-stu-id="73519-116">This command gets all the container registries in the subscription.</span></span>

## <span data-ttu-id="73519-117">參數</span><span class="sxs-lookup"><span data-stu-id="73519-117">PARAMETERS</span></span>

### <span data-ttu-id="73519-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73519-118">-DefaultProfile</span></span>
<span data-ttu-id="73519-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="73519-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="73519-120">-IncludeDetail</span><span class="sxs-lookup"><span data-stu-id="73519-120">-IncludeDetail</span></span>
<span data-ttu-id="73519-121">顯示容器註冊表的更多詳細資料。</span><span class="sxs-lookup"><span data-stu-id="73519-121">Show more details about the container registry.</span></span>

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

### <span data-ttu-id="73519-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="73519-122">-Name</span></span>
<span data-ttu-id="73519-123">容器註冊表名稱。</span><span class="sxs-lookup"><span data-stu-id="73519-123">Container Registry Name.</span></span>

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

### <span data-ttu-id="73519-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73519-124">-ResourceGroupName</span></span>
<span data-ttu-id="73519-125">資源組名。</span><span class="sxs-lookup"><span data-stu-id="73519-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="73519-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="73519-126">-ResourceId</span></span>
<span data-ttu-id="73519-127">容器登錄資源識別碼</span><span class="sxs-lookup"><span data-stu-id="73519-127">The container registry resource id</span></span>

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

### <span data-ttu-id="73519-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73519-128">CommonParameters</span></span>
<span data-ttu-id="73519-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="73519-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73519-130">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="73519-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73519-131">輸入</span><span class="sxs-lookup"><span data-stu-id="73519-131">INPUTS</span></span>

### <span data-ttu-id="73519-132">System.String</span><span class="sxs-lookup"><span data-stu-id="73519-132">System.String</span></span>

## <span data-ttu-id="73519-133">輸出</span><span class="sxs-lookup"><span data-stu-id="73519-133">OUTPUTS</span></span>

### <span data-ttu-id="73519-134">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="73519-134">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="73519-135">筆記</span><span class="sxs-lookup"><span data-stu-id="73519-135">NOTES</span></span>

## <span data-ttu-id="73519-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="73519-136">RELATED LINKS</span></span>

[<span data-ttu-id="73519-137">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="73519-137">New-AzContainerRegistry</span></span>](New-AzContainerRegistry.md)

[<span data-ttu-id="73519-138">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="73519-138">Update-AzContainerRegistry</span></span>](Update-AzContainerRegistry.md)

[<span data-ttu-id="73519-139">Remove-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="73519-139">Remove-AzContainerRegistry</span></span>](Remove-AzContainerRegistry.md)

