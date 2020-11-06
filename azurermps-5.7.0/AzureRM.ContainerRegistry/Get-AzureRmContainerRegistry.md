---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/get-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistry.md
ms.openlocfilehash: dc1b35831de68ad31877be05610d1b075b27452f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455460"
---
# <span data-ttu-id="19442-101">Get-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="19442-101">Get-AzureRmContainerRegistry</span></span>

## <span data-ttu-id="19442-102">摘要</span><span class="sxs-lookup"><span data-stu-id="19442-102">SYNOPSIS</span></span>
<span data-ttu-id="19442-103">取得容器註冊。</span><span class="sxs-lookup"><span data-stu-id="19442-103">Gets a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="19442-104">句法</span><span class="sxs-lookup"><span data-stu-id="19442-104">SYNTAX</span></span>

### <span data-ttu-id="19442-105">ListRegistriesParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="19442-105">ListRegistriesParameterSet (Default)</span></span>
```
Get-AzureRmContainerRegistry [[-ResourceGroupName] <String>] [-IncludeDetail]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="19442-106">RegistryNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="19442-106">RegistryNameParameterSet</span></span>
```
Get-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-IncludeDetail]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="19442-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="19442-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmContainerRegistry [-IncludeDetail] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="19442-108">說明</span><span class="sxs-lookup"><span data-stu-id="19442-108">DESCRIPTION</span></span>
<span data-ttu-id="19442-109">Get-AzureRmContainerRegistry Cmdlet 會取得指定的容器登錄，或資源群組或訂閱中的所有容器註冊機構。</span><span class="sxs-lookup"><span data-stu-id="19442-109">The Get-AzureRmContainerRegistry cmdlet gets a specified container registry or all the container registries in a resource group or the subscription.</span></span>

## <span data-ttu-id="19442-110">示例</span><span class="sxs-lookup"><span data-stu-id="19442-110">EXAMPLES</span></span>

### <span data-ttu-id="19442-111">範例1：取得指定的樹枝 registry</span><span class="sxs-lookup"><span data-stu-id="19442-111">Example 1: Get a specified container registry</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"

   Container registry location: westus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="19442-112">這個命令會取得指定的容器註冊。</span><span class="sxs-lookup"><span data-stu-id="19442-112">This command gets the specified container registry.</span></span>

### <span data-ttu-id="19442-113">範例2：取得資源群組中的所有容器註冊表</span><span class="sxs-lookup"><span data-stu-id="19442-113">Example 2: Get all the container registries in a resource group</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup"

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

<span data-ttu-id="19442-114">這個命令會取得資源群組中的所有容器註冊表。</span><span class="sxs-lookup"><span data-stu-id="19442-114">This command gets all the container registries in a resource group.</span></span>

### <span data-ttu-id="19442-115">範例3：取得訂閱中的所有容器註冊表</span><span class="sxs-lookup"><span data-stu-id="19442-115">Example 3:  Get all the container registries in the subscription</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistry

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

<span data-ttu-id="19442-116">這個命令會取得訂閱中的所有容器註冊表。</span><span class="sxs-lookup"><span data-stu-id="19442-116">This command gets all the container registries in the subscription.</span></span>

## <span data-ttu-id="19442-117">參數</span><span class="sxs-lookup"><span data-stu-id="19442-117">PARAMETERS</span></span>

### <span data-ttu-id="19442-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="19442-118">-Name</span></span>
<span data-ttu-id="19442-119">容器登錄名。</span><span class="sxs-lookup"><span data-stu-id="19442-119">Container Registry Name.</span></span>

```yaml
Type: String
Parameter Sets: RegistryNameParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19442-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19442-120">-ResourceGroupName</span></span>
<span data-ttu-id="19442-121">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="19442-121">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: ListRegistriesParameterSet
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: RegistryNameParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19442-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19442-122">-DefaultProfile</span></span>
<span data-ttu-id="19442-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="19442-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="19442-124">-IncludeDetail</span><span class="sxs-lookup"><span data-stu-id="19442-124">-IncludeDetail</span></span>
<span data-ttu-id="19442-125">顯示更多關於容器註冊表的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="19442-125">Show more details about the container registry.</span></span>

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

### <span data-ttu-id="19442-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="19442-126">-ResourceId</span></span>
<span data-ttu-id="19442-127">容器登錄資源識別碼</span><span class="sxs-lookup"><span data-stu-id="19442-127">The container registry resource id</span></span>

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

### <span data-ttu-id="19442-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19442-128">CommonParameters</span></span>
<span data-ttu-id="19442-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="19442-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19442-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="19442-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19442-131">輸入</span><span class="sxs-lookup"><span data-stu-id="19442-131">INPUTS</span></span>

### <span data-ttu-id="19442-132">所有</span><span class="sxs-lookup"><span data-stu-id="19442-132">None</span></span>
<span data-ttu-id="19442-133">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="19442-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="19442-134">輸出</span><span class="sxs-lookup"><span data-stu-id="19442-134">OUTPUTS</span></span>

### <span data-ttu-id="19442-135">PSContainerRegistry 中的 ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="19442-135">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="19442-136">筆記</span><span class="sxs-lookup"><span data-stu-id="19442-136">NOTES</span></span>

## <span data-ttu-id="19442-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="19442-137">RELATED LINKS</span></span>

[<span data-ttu-id="19442-138">新-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="19442-138">New-AzureRmContainerRegistry</span></span>](New-AzureRmContainerRegistry.md)

[<span data-ttu-id="19442-139">更新-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="19442-139">Update-AzureRmContainerRegistry</span></span>](Update-AzureRmContainerRegistry.md)

[<span data-ttu-id="19442-140">移除-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="19442-140">Remove-AzureRmContainerRegistry</span></span>](Remove-AzureRmContainerRegistry.md)

