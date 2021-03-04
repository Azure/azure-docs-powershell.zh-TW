---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/get-azcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryCredential.md
ms.openlocfilehash: 5e20ae556cba16263d8b650de869b174236ccbd5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915561"
---
# <span data-ttu-id="9e5e3-101">Get-AzContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="9e5e3-101">Get-AzContainerRegistryCredential</span></span>

## <span data-ttu-id="9e5e3-102">簡介</span><span class="sxs-lookup"><span data-stu-id="9e5e3-102">SYNOPSIS</span></span>
<span data-ttu-id="9e5e3-103">獲得容器登錄的登入認證。</span><span class="sxs-lookup"><span data-stu-id="9e5e3-103">Gets the login credentials for a container registry.</span></span>

## <span data-ttu-id="9e5e3-104">語法</span><span class="sxs-lookup"><span data-stu-id="9e5e3-104">SYNTAX</span></span>

### <span data-ttu-id="9e5e3-105">NameResourceGroupParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="9e5e3-105">NameResourceGroupParameterSet (Default)</span></span>
```
Get-AzContainerRegistryCredential [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e5e3-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e5e3-106">RegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryCredential -Registry <PSContainerRegistry> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9e5e3-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e5e3-107">ResourceIdParameterSet</span></span>
```
Get-AzContainerRegistryCredential -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9e5e3-108">描述</span><span class="sxs-lookup"><span data-stu-id="9e5e3-108">DESCRIPTION</span></span>
<span data-ttu-id="9e5e3-109">此Get-AzContainerRegistryCredential Cmdlet 會獲得容器登錄的登入認證。</span><span class="sxs-lookup"><span data-stu-id="9e5e3-109">The Get-AzContainerRegistryCredential cmdlet gets the login credentials for a container registry.</span></span>

## <span data-ttu-id="9e5e3-110">例子</span><span class="sxs-lookup"><span data-stu-id="9e5e3-110">EXAMPLES</span></span>

### <span data-ttu-id="9e5e3-111">範例 1：取得容器登錄的登入認證</span><span class="sxs-lookup"><span data-stu-id="9e5e3-111">Example 1: Get the login credentials for a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryCredential -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"

Username   Password                         Password2
--------   --------                         ---------
MyRegistry +Y+==B==KdT=YV=ZgH=p/zQ/e1sNQq/d //JRPkgxx+r+z/ztU=R//E==vum=pRKL
```

<span data-ttu-id="9e5e3-112">此命令會獲得指定容器登錄的登入認證。</span><span class="sxs-lookup"><span data-stu-id="9e5e3-112">This command gets the login credentials for the specified container registry.</span></span>
<span data-ttu-id="9e5e3-113">系統管理使用者必須啟用容器登錄 \` MyRegistry \` 才能取得登入認證。</span><span class="sxs-lookup"><span data-stu-id="9e5e3-113">Admin user has to be enabled for the container registry \`MyRegistry\` to get login credentials.</span></span>

## <span data-ttu-id="9e5e3-114">參數</span><span class="sxs-lookup"><span data-stu-id="9e5e3-114">PARAMETERS</span></span>

### <span data-ttu-id="9e5e3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e5e3-115">-DefaultProfile</span></span>
<span data-ttu-id="9e5e3-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="9e5e3-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9e5e3-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="9e5e3-117">-Name</span></span>
<span data-ttu-id="9e5e3-118">容器註冊表名稱。</span><span class="sxs-lookup"><span data-stu-id="9e5e3-118">Container Registry Name.</span></span>

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

### <span data-ttu-id="9e5e3-119">-Registry</span><span class="sxs-lookup"><span data-stu-id="9e5e3-119">-Registry</span></span>
<span data-ttu-id="9e5e3-120">Container Registry 物件。</span><span class="sxs-lookup"><span data-stu-id="9e5e3-120">Container Registry Object.</span></span>

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

### <span data-ttu-id="9e5e3-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e5e3-121">-ResourceGroupName</span></span>
<span data-ttu-id="9e5e3-122">資源組名。</span><span class="sxs-lookup"><span data-stu-id="9e5e3-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="9e5e3-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9e5e3-123">-ResourceId</span></span>
<span data-ttu-id="9e5e3-124">容器登錄資源識別碼</span><span class="sxs-lookup"><span data-stu-id="9e5e3-124">The container registry resource id</span></span>

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

### <span data-ttu-id="9e5e3-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e5e3-125">CommonParameters</span></span>
<span data-ttu-id="9e5e3-126">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="9e5e3-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e5e3-127">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9e5e3-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e5e3-128">輸入</span><span class="sxs-lookup"><span data-stu-id="9e5e3-128">INPUTS</span></span>

### <span data-ttu-id="9e5e3-129">System.String</span><span class="sxs-lookup"><span data-stu-id="9e5e3-129">System.String</span></span>

## <span data-ttu-id="9e5e3-130">輸出</span><span class="sxs-lookup"><span data-stu-id="9e5e3-130">OUTPUTS</span></span>

### <span data-ttu-id="9e5e3-131">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="9e5e3-131">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span></span>

## <span data-ttu-id="9e5e3-132">筆記</span><span class="sxs-lookup"><span data-stu-id="9e5e3-132">NOTES</span></span>

## <span data-ttu-id="9e5e3-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="9e5e3-133">RELATED LINKS</span></span>

[<span data-ttu-id="9e5e3-134">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="9e5e3-134">New-AzContainerRegistry</span></span>](New-AzContainerRegistry.md)

[<span data-ttu-id="9e5e3-135">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="9e5e3-135">Update-AzContainerRegistry</span></span>](Update-AzContainerRegistry.md)

[<span data-ttu-id="9e5e3-136">Update-AzContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="9e5e3-136">Update-AzContainerRegistryCredential</span></span>](Update-AzContainerRegistryCredential.md)

