---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/update-azurermcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistryCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistryCredential.md
ms.openlocfilehash: 836e8983a9d2e6c7ff21444f0da7b3bf85c1b1d4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456103"
---
# <span data-ttu-id="a376a-101">Update-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="a376a-101">Update-AzureRmContainerRegistryCredential</span></span>

## <span data-ttu-id="a376a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a376a-102">SYNOPSIS</span></span>
<span data-ttu-id="a376a-103">重新產生容器註冊的登入認證。</span><span class="sxs-lookup"><span data-stu-id="a376a-103">Regenerates a login credential for a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a376a-104">句法</span><span class="sxs-lookup"><span data-stu-id="a376a-104">SYNTAX</span></span>

### <span data-ttu-id="a376a-105">NameResourceGroupParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="a376a-105">NameResourceGroupParameterSet (Default)</span></span>
```
Update-AzureRmContainerRegistryCredential [-ResourceGroupName] <String> [-Name] <String>
 -PasswordName <PasswordName> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a376a-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a376a-106">RegistryObjectParameterSet</span></span>
```
Update-AzureRmContainerRegistryCredential -Registry <PSContainerRegistry> -PasswordName <PasswordName>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a376a-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a376a-107">ResourceIdParameterSet</span></span>
```
Update-AzureRmContainerRegistryCredential -PasswordName <PasswordName> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a376a-108">說明</span><span class="sxs-lookup"><span data-stu-id="a376a-108">DESCRIPTION</span></span>
<span data-ttu-id="a376a-109">Update-AzureRmContainerRegistryCredential Cmdlet 會為容器註冊重新產生登入認證。</span><span class="sxs-lookup"><span data-stu-id="a376a-109">The Update-AzureRmContainerRegistryCredential cmdlet regenerates a login credential for a container registry.</span></span>

## <span data-ttu-id="a376a-110">示例</span><span class="sxs-lookup"><span data-stu-id="a376a-110">EXAMPLES</span></span>

### <span data-ttu-id="a376a-111">範例1：為容器註冊表重新產生登入認證</span><span class="sxs-lookup"><span data-stu-id="a376a-111">Example 1: Regenerate a login credential for a container registry</span></span>
```powershell
PS C:\>Update-AzureRmContainerRegistryCredential -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -PasswordName "Password"

Username   Password                         Password2
--------   --------                         ---------
MyRegistry ++q/=K9+RH/+hwg2+3A=N+/w=J/12Ph9 //JRPkgxx+r+z/ztU=R//E==vum=pRKL
```

<span data-ttu-id="a376a-112">這個命令會為指定的容器註冊表重新產生登入認證。</span><span class="sxs-lookup"><span data-stu-id="a376a-112">This command regenerates a login credential for the specified container registry.</span></span>
<span data-ttu-id="a376a-113">管理員使用者必須啟用容器 \` \` 登錄 MyRegistry，才能重新產生登入認證。</span><span class="sxs-lookup"><span data-stu-id="a376a-113">Admin user has to be enabled for the container registry \`MyRegistry\` to regenerate login credentials.</span></span>

## <span data-ttu-id="a376a-114">參數</span><span class="sxs-lookup"><span data-stu-id="a376a-114">PARAMETERS</span></span>

### <span data-ttu-id="a376a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a376a-115">-DefaultProfile</span></span>
<span data-ttu-id="a376a-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="a376a-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a376a-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="a376a-117">-Name</span></span>
<span data-ttu-id="a376a-118">容器登錄名。</span><span class="sxs-lookup"><span data-stu-id="a376a-118">Container Registry Name.</span></span>

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

### <span data-ttu-id="a376a-119">-PasswordName</span><span class="sxs-lookup"><span data-stu-id="a376a-119">-PasswordName</span></span>
<span data-ttu-id="a376a-120">要重新產生的密碼的名稱。</span><span class="sxs-lookup"><span data-stu-id="a376a-120">The name of password to regenerate.</span></span>
<span data-ttu-id="a376a-121">允許的值： password、password2。</span><span class="sxs-lookup"><span data-stu-id="a376a-121">Allowed values: password, password2.</span></span>

```yaml
Type: Microsoft.Azure.Management.ContainerRegistry.Models.PasswordName
Parameter Sets: (All)
Aliases:
Accepted values: password, password2

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a376a-122">-Registry</span><span class="sxs-lookup"><span data-stu-id="a376a-122">-Registry</span></span>
<span data-ttu-id="a376a-123">分枝 Registry 物件。</span><span class="sxs-lookup"><span data-stu-id="a376a-123">Container Registry Object.</span></span>

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

### <span data-ttu-id="a376a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a376a-124">-ResourceGroupName</span></span>
<span data-ttu-id="a376a-125">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="a376a-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="a376a-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a376a-126">-ResourceId</span></span>
<span data-ttu-id="a376a-127">容器登錄資源識別碼</span><span class="sxs-lookup"><span data-stu-id="a376a-127">The container registry resource id</span></span>

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

### <span data-ttu-id="a376a-128">-確認</span><span class="sxs-lookup"><span data-stu-id="a376a-128">-Confirm</span></span>
<span data-ttu-id="a376a-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a376a-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a376a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a376a-130">-WhatIf</span></span>
<span data-ttu-id="a376a-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a376a-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a376a-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a376a-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a376a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a376a-133">CommonParameters</span></span>
<span data-ttu-id="a376a-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a376a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a376a-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a376a-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a376a-136">輸入</span><span class="sxs-lookup"><span data-stu-id="a376a-136">INPUTS</span></span>

### <span data-ttu-id="a376a-137">PSContainerRegistry 中的 ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="a376a-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>
<span data-ttu-id="a376a-138">參數： Registry (ByValue) </span><span class="sxs-lookup"><span data-stu-id="a376a-138">Parameters: Registry (ByValue)</span></span>

### <span data-ttu-id="a376a-139">System.object</span><span class="sxs-lookup"><span data-stu-id="a376a-139">System.String</span></span>

## <span data-ttu-id="a376a-140">輸出</span><span class="sxs-lookup"><span data-stu-id="a376a-140">OUTPUTS</span></span>

### <span data-ttu-id="a376a-141">PSContainerRegistryCredential 中的 ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="a376a-141">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span></span>

## <span data-ttu-id="a376a-142">筆記</span><span class="sxs-lookup"><span data-stu-id="a376a-142">NOTES</span></span>

## <span data-ttu-id="a376a-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="a376a-143">RELATED LINKS</span></span>

[<span data-ttu-id="a376a-144">新-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="a376a-144">New-AzureRmContainerRegistry</span></span>](New-AzureRmContainerRegistry.md)

[<span data-ttu-id="a376a-145">更新-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="a376a-145">Update-AzureRmContainerRegistry</span></span>](Update-AzureRmContainerRegistry.md)

[<span data-ttu-id="a376a-146">AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="a376a-146">Get-AzureRmContainerRegistryCredential</span></span>](Get-AzureRmContainerRegistryCredential.md)

