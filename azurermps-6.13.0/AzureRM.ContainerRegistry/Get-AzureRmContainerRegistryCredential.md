---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/get-azurermcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryCredential.md
ms.openlocfilehash: 37ca6fad019814c476f48d1f086a430db75afb99
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93443935"
---
# <span data-ttu-id="259f8-101">Get-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="259f8-101">Get-AzureRmContainerRegistryCredential</span></span>

## <span data-ttu-id="259f8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="259f8-102">SYNOPSIS</span></span>
<span data-ttu-id="259f8-103">取得容器註冊的登入認證。</span><span class="sxs-lookup"><span data-stu-id="259f8-103">Gets the login credentials for a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="259f8-104">句法</span><span class="sxs-lookup"><span data-stu-id="259f8-104">SYNTAX</span></span>

### <span data-ttu-id="259f8-105">NameResourceGroupParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="259f8-105">NameResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmContainerRegistryCredential [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="259f8-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="259f8-106">RegistryObjectParameterSet</span></span>
```
Get-AzureRmContainerRegistryCredential -Registry <PSContainerRegistry>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="259f8-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="259f8-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmContainerRegistryCredential -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="259f8-108">說明</span><span class="sxs-lookup"><span data-stu-id="259f8-108">DESCRIPTION</span></span>
<span data-ttu-id="259f8-109">Get-AzureRmContainerRegistryCredential Cmdlet 會取得容器註冊的登入認證。</span><span class="sxs-lookup"><span data-stu-id="259f8-109">The Get-AzureRmContainerRegistryCredential cmdlet gets the login credentials for a container registry.</span></span>

## <span data-ttu-id="259f8-110">示例</span><span class="sxs-lookup"><span data-stu-id="259f8-110">EXAMPLES</span></span>

### <span data-ttu-id="259f8-111">範例1：取得容器註冊的登入認證</span><span class="sxs-lookup"><span data-stu-id="259f8-111">Example 1: Get the login credentials for a container registry</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistryCredential -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"

Username   Password                         Password2
--------   --------                         ---------
MyRegistry +Y+==B==KdT=YV=ZgH=p/zQ/e1sNQq/d //JRPkgxx+r+z/ztU=R//E==vum=pRKL
```

<span data-ttu-id="259f8-112">這個命令會取得指定之容器註冊表的登入認證。</span><span class="sxs-lookup"><span data-stu-id="259f8-112">This command gets the login credentials for the specified container registry.</span></span>
<span data-ttu-id="259f8-113">管理員使用者必須啟用容器 \` \` 登錄 MyRegistry，才能取得登入認證。</span><span class="sxs-lookup"><span data-stu-id="259f8-113">Admin user has to be enabled for the container registry \`MyRegistry\` to get login credentials.</span></span>

## <span data-ttu-id="259f8-114">參數</span><span class="sxs-lookup"><span data-stu-id="259f8-114">PARAMETERS</span></span>

### <span data-ttu-id="259f8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="259f8-115">-DefaultProfile</span></span>
<span data-ttu-id="259f8-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="259f8-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="259f8-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="259f8-117">-Name</span></span>
<span data-ttu-id="259f8-118">容器登錄名。</span><span class="sxs-lookup"><span data-stu-id="259f8-118">Container Registry Name.</span></span>

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

### <span data-ttu-id="259f8-119">-Registry</span><span class="sxs-lookup"><span data-stu-id="259f8-119">-Registry</span></span>
<span data-ttu-id="259f8-120">分枝 Registry 物件。</span><span class="sxs-lookup"><span data-stu-id="259f8-120">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="259f8-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="259f8-121">-ResourceGroupName</span></span>
<span data-ttu-id="259f8-122">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="259f8-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="259f8-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="259f8-123">-ResourceId</span></span>
<span data-ttu-id="259f8-124">容器登錄資源識別碼</span><span class="sxs-lookup"><span data-stu-id="259f8-124">The container registry resource id</span></span>

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

### <span data-ttu-id="259f8-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="259f8-125">CommonParameters</span></span>
<span data-ttu-id="259f8-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="259f8-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="259f8-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="259f8-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="259f8-128">輸入</span><span class="sxs-lookup"><span data-stu-id="259f8-128">INPUTS</span></span>

### <span data-ttu-id="259f8-129">System.object</span><span class="sxs-lookup"><span data-stu-id="259f8-129">System.String</span></span>

## <span data-ttu-id="259f8-130">輸出</span><span class="sxs-lookup"><span data-stu-id="259f8-130">OUTPUTS</span></span>

### <span data-ttu-id="259f8-131">PSContainerRegistryCredential 中的 ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="259f8-131">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span></span>

## <span data-ttu-id="259f8-132">筆記</span><span class="sxs-lookup"><span data-stu-id="259f8-132">NOTES</span></span>

## <span data-ttu-id="259f8-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="259f8-133">RELATED LINKS</span></span>

[<span data-ttu-id="259f8-134">新-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="259f8-134">New-AzureRmContainerRegistry</span></span>](New-AzureRmContainerRegistry.md)

[<span data-ttu-id="259f8-135">更新-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="259f8-135">Update-AzureRmContainerRegistry</span></span>](Update-AzureRmContainerRegistry.md)

[<span data-ttu-id="259f8-136">更新-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="259f8-136">Update-AzureRmContainerRegistryCredential</span></span>](Update-AzureRmContainerRegistryCredential.md)

