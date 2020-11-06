---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/get-azurermcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryCredential.md
ms.openlocfilehash: 68ef1cf00adeec785faf3c3f43ff2e7dbcaafbc5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455459"
---
# <span data-ttu-id="af9ad-101">Get-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="af9ad-101">Get-AzureRmContainerRegistryCredential</span></span>

## <span data-ttu-id="af9ad-102">摘要</span><span class="sxs-lookup"><span data-stu-id="af9ad-102">SYNOPSIS</span></span>
<span data-ttu-id="af9ad-103">取得容器註冊的登入認證。</span><span class="sxs-lookup"><span data-stu-id="af9ad-103">Gets the login credentials for a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="af9ad-104">句法</span><span class="sxs-lookup"><span data-stu-id="af9ad-104">SYNTAX</span></span>

### <span data-ttu-id="af9ad-105">NameResourceGroupParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="af9ad-105">NameResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmContainerRegistryCredential [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="af9ad-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="af9ad-106">RegistryObjectParameterSet</span></span>
```
Get-AzureRmContainerRegistryCredential -Registry <PSContainerRegistry>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="af9ad-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="af9ad-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmContainerRegistryCredential -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="af9ad-108">說明</span><span class="sxs-lookup"><span data-stu-id="af9ad-108">DESCRIPTION</span></span>
<span data-ttu-id="af9ad-109">Get-AzureRmContainerRegistryCredential Cmdlet 會取得容器註冊的登入認證。</span><span class="sxs-lookup"><span data-stu-id="af9ad-109">The Get-AzureRmContainerRegistryCredential cmdlet gets the login credentials for a container registry.</span></span>

## <span data-ttu-id="af9ad-110">示例</span><span class="sxs-lookup"><span data-stu-id="af9ad-110">EXAMPLES</span></span>

### <span data-ttu-id="af9ad-111">範例1：取得容器註冊的登入認證</span><span class="sxs-lookup"><span data-stu-id="af9ad-111">Example 1: Get the login credentials for a container registry</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistryCredential -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"

Username   Password                         Password2
--------   --------                         ---------
MyRegistry +Y+==B==KdT=YV=ZgH=p/zQ/e1sNQq/d //JRPkgxx+r+z/ztU=R//E==vum=pRKL
```

<span data-ttu-id="af9ad-112">這個命令會取得指定之容器註冊表的登入認證。</span><span class="sxs-lookup"><span data-stu-id="af9ad-112">This command gets the login credentials for the specified container registry.</span></span>
<span data-ttu-id="af9ad-113">管理員使用者必須啟用容器 \` \` 登錄 MyRegistry，才能取得登入認證。</span><span class="sxs-lookup"><span data-stu-id="af9ad-113">Admin user has to be enabled for the container registry \`MyRegistry\` to get login credentials.</span></span>

## <span data-ttu-id="af9ad-114">參數</span><span class="sxs-lookup"><span data-stu-id="af9ad-114">PARAMETERS</span></span>

### <span data-ttu-id="af9ad-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="af9ad-115">-Name</span></span>
<span data-ttu-id="af9ad-116">容器登錄名。</span><span class="sxs-lookup"><span data-stu-id="af9ad-116">Container Registry Name.</span></span>

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

### <span data-ttu-id="af9ad-117">-Registry</span><span class="sxs-lookup"><span data-stu-id="af9ad-117">-Registry</span></span>
<span data-ttu-id="af9ad-118">分枝 Registry 物件。</span><span class="sxs-lookup"><span data-stu-id="af9ad-118">Container Registry Object.</span></span>

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

### <span data-ttu-id="af9ad-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af9ad-119">-ResourceGroupName</span></span>
<span data-ttu-id="af9ad-120">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="af9ad-120">Resource Group Name.</span></span>

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

### <span data-ttu-id="af9ad-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af9ad-121">-DefaultProfile</span></span>
<span data-ttu-id="af9ad-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="af9ad-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="af9ad-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="af9ad-123">-ResourceId</span></span>
<span data-ttu-id="af9ad-124">容器登錄資源識別碼</span><span class="sxs-lookup"><span data-stu-id="af9ad-124">The container registry resource id</span></span>

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

### <span data-ttu-id="af9ad-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af9ad-125">CommonParameters</span></span>
<span data-ttu-id="af9ad-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="af9ad-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af9ad-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="af9ad-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af9ad-128">輸入</span><span class="sxs-lookup"><span data-stu-id="af9ad-128">INPUTS</span></span>

### <span data-ttu-id="af9ad-129">PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="af9ad-129">PSContainerRegistry</span></span>
<span data-ttu-id="af9ad-130">參數 "Registry" 接受管線中 "PSContainerRegistry" 類型的值</span><span class="sxs-lookup"><span data-stu-id="af9ad-130">Parameter 'Registry' accepts value of type 'PSContainerRegistry' from the pipeline</span></span>

## <span data-ttu-id="af9ad-131">輸出</span><span class="sxs-lookup"><span data-stu-id="af9ad-131">OUTPUTS</span></span>

### <span data-ttu-id="af9ad-132">PSContainerRegistryCredential 中的 ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="af9ad-132">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span></span>

## <span data-ttu-id="af9ad-133">筆記</span><span class="sxs-lookup"><span data-stu-id="af9ad-133">NOTES</span></span>

## <span data-ttu-id="af9ad-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="af9ad-134">RELATED LINKS</span></span>

[<span data-ttu-id="af9ad-135">新-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="af9ad-135">New-AzureRmContainerRegistry</span></span>](New-AzureRmContainerRegistry.md)

[<span data-ttu-id="af9ad-136">更新-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="af9ad-136">Update-AzureRmContainerRegistry</span></span>](Update-AzureRmContainerRegistry.md)

[<span data-ttu-id="af9ad-137">更新-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="af9ad-137">Update-AzureRmContainerRegistryCredential</span></span>](Update-AzureRmContainerRegistryCredential.md)

