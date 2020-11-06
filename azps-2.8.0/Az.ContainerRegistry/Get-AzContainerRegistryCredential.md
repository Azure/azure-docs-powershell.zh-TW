---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryCredential.md
ms.openlocfilehash: 89b3f47953c4074088c1ae5e2cf8e5f51ff383e9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613076"
---
# <span data-ttu-id="70e41-101">Get-AzContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="70e41-101">Get-AzContainerRegistryCredential</span></span>

## <span data-ttu-id="70e41-102">摘要</span><span class="sxs-lookup"><span data-stu-id="70e41-102">SYNOPSIS</span></span>
<span data-ttu-id="70e41-103">取得容器註冊的登入認證。</span><span class="sxs-lookup"><span data-stu-id="70e41-103">Gets the login credentials for a container registry.</span></span>

## <span data-ttu-id="70e41-104">句法</span><span class="sxs-lookup"><span data-stu-id="70e41-104">SYNTAX</span></span>

### <span data-ttu-id="70e41-105">NameResourceGroupParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="70e41-105">NameResourceGroupParameterSet (Default)</span></span>
```
Get-AzContainerRegistryCredential [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="70e41-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="70e41-106">RegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryCredential -Registry <PSContainerRegistry> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="70e41-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="70e41-107">ResourceIdParameterSet</span></span>
```
Get-AzContainerRegistryCredential -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="70e41-108">說明</span><span class="sxs-lookup"><span data-stu-id="70e41-108">DESCRIPTION</span></span>
<span data-ttu-id="70e41-109">Get-AzContainerRegistryCredential Cmdlet 會取得容器註冊的登入認證。</span><span class="sxs-lookup"><span data-stu-id="70e41-109">The Get-AzContainerRegistryCredential cmdlet gets the login credentials for a container registry.</span></span>

## <span data-ttu-id="70e41-110">示例</span><span class="sxs-lookup"><span data-stu-id="70e41-110">EXAMPLES</span></span>

### <span data-ttu-id="70e41-111">範例1：取得容器註冊的登入認證</span><span class="sxs-lookup"><span data-stu-id="70e41-111">Example 1: Get the login credentials for a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryCredential -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"

Username   Password                         Password2
--------   --------                         ---------
MyRegistry +Y+==B==KdT=YV=ZgH=p/zQ/e1sNQq/d //JRPkgxx+r+z/ztU=R//E==vum=pRKL
```

<span data-ttu-id="70e41-112">這個命令會取得指定之容器註冊表的登入認證。</span><span class="sxs-lookup"><span data-stu-id="70e41-112">This command gets the login credentials for the specified container registry.</span></span>
<span data-ttu-id="70e41-113">管理員使用者必須啟用容器 \` \` 登錄 MyRegistry，才能取得登入認證。</span><span class="sxs-lookup"><span data-stu-id="70e41-113">Admin user has to be enabled for the container registry \`MyRegistry\` to get login credentials.</span></span>

## <span data-ttu-id="70e41-114">參數</span><span class="sxs-lookup"><span data-stu-id="70e41-114">PARAMETERS</span></span>

### <span data-ttu-id="70e41-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70e41-115">-DefaultProfile</span></span>
<span data-ttu-id="70e41-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="70e41-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="70e41-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="70e41-117">-Name</span></span>
<span data-ttu-id="70e41-118">容器登錄名。</span><span class="sxs-lookup"><span data-stu-id="70e41-118">Container Registry Name.</span></span>

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

### <span data-ttu-id="70e41-119">-Registry</span><span class="sxs-lookup"><span data-stu-id="70e41-119">-Registry</span></span>
<span data-ttu-id="70e41-120">分枝 Registry 物件。</span><span class="sxs-lookup"><span data-stu-id="70e41-120">Container Registry Object.</span></span>

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

### <span data-ttu-id="70e41-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70e41-121">-ResourceGroupName</span></span>
<span data-ttu-id="70e41-122">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="70e41-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="70e41-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="70e41-123">-ResourceId</span></span>
<span data-ttu-id="70e41-124">容器登錄資源識別碼</span><span class="sxs-lookup"><span data-stu-id="70e41-124">The container registry resource id</span></span>

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

### <span data-ttu-id="70e41-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70e41-125">CommonParameters</span></span>
<span data-ttu-id="70e41-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="70e41-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70e41-127">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="70e41-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70e41-128">輸入</span><span class="sxs-lookup"><span data-stu-id="70e41-128">INPUTS</span></span>

### <span data-ttu-id="70e41-129">System.object</span><span class="sxs-lookup"><span data-stu-id="70e41-129">System.String</span></span>

## <span data-ttu-id="70e41-130">輸出</span><span class="sxs-lookup"><span data-stu-id="70e41-130">OUTPUTS</span></span>

### <span data-ttu-id="70e41-131">PSContainerRegistryCredential 中的 ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="70e41-131">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span></span>

## <span data-ttu-id="70e41-132">筆記</span><span class="sxs-lookup"><span data-stu-id="70e41-132">NOTES</span></span>

## <span data-ttu-id="70e41-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="70e41-133">RELATED LINKS</span></span>

[<span data-ttu-id="70e41-134">新-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="70e41-134">New-AzContainerRegistry</span></span>](New-AzContainerRegistry.md)

[<span data-ttu-id="70e41-135">更新-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="70e41-135">Update-AzContainerRegistry</span></span>](Update-AzContainerRegistry.md)

[<span data-ttu-id="70e41-136">更新-AzContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="70e41-136">Update-AzContainerRegistryCredential</span></span>](Update-AzContainerRegistryCredential.md)
