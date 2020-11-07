---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/update-azcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryCredential.md
ms.openlocfilehash: d8e5f36366df16dd7b0d03fb07f948e436c0a919
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93797309"
---
# <span data-ttu-id="23487-101">Update-AzContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="23487-101">Update-AzContainerRegistryCredential</span></span>

## <span data-ttu-id="23487-102">摘要</span><span class="sxs-lookup"><span data-stu-id="23487-102">SYNOPSIS</span></span>
<span data-ttu-id="23487-103">重新產生容器註冊的登入認證。</span><span class="sxs-lookup"><span data-stu-id="23487-103">Regenerates a login credential for a container registry.</span></span>

## <span data-ttu-id="23487-104">句法</span><span class="sxs-lookup"><span data-stu-id="23487-104">SYNTAX</span></span>

### <span data-ttu-id="23487-105">NameResourceGroupParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="23487-105">NameResourceGroupParameterSet (Default)</span></span>
```
Update-AzContainerRegistryCredential [-ResourceGroupName] <String> [-Name] <String>
 -PasswordName <PasswordName> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="23487-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="23487-106">RegistryObjectParameterSet</span></span>
```
Update-AzContainerRegistryCredential -Registry <PSContainerRegistry> -PasswordName <PasswordName>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23487-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="23487-107">ResourceIdParameterSet</span></span>
```
Update-AzContainerRegistryCredential -PasswordName <PasswordName> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23487-108">說明</span><span class="sxs-lookup"><span data-stu-id="23487-108">DESCRIPTION</span></span>
<span data-ttu-id="23487-109">Update-AzContainerRegistryCredential Cmdlet 會為容器註冊重新產生登入認證。</span><span class="sxs-lookup"><span data-stu-id="23487-109">The Update-AzContainerRegistryCredential cmdlet regenerates a login credential for a container registry.</span></span>

## <span data-ttu-id="23487-110">示例</span><span class="sxs-lookup"><span data-stu-id="23487-110">EXAMPLES</span></span>

### <span data-ttu-id="23487-111">範例1：為容器註冊表重新產生登入認證</span><span class="sxs-lookup"><span data-stu-id="23487-111">Example 1: Regenerate a login credential for a container registry</span></span>
```powershell
PS C:\>Update-AzContainerRegistryCredential -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -PasswordName "Password"

Username   Password                         Password2
--------   --------                         ---------
MyRegistry ++q/=K9+RH/+hwg2+3A=N+/w=J/12Ph9 //JRPkgxx+r+z/ztU=R//E==vum=pRKL
```

<span data-ttu-id="23487-112">這個命令會為指定的容器註冊表重新產生登入認證。</span><span class="sxs-lookup"><span data-stu-id="23487-112">This command regenerates a login credential for the specified container registry.</span></span>
<span data-ttu-id="23487-113">管理員使用者必須啟用容器 \` \` 登錄 MyRegistry，才能重新產生登入認證。</span><span class="sxs-lookup"><span data-stu-id="23487-113">Admin user has to be enabled for the container registry \`MyRegistry\` to regenerate login credentials.</span></span>

## <span data-ttu-id="23487-114">參數</span><span class="sxs-lookup"><span data-stu-id="23487-114">PARAMETERS</span></span>

### <span data-ttu-id="23487-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23487-115">-DefaultProfile</span></span>
<span data-ttu-id="23487-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="23487-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="23487-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="23487-117">-Name</span></span>
<span data-ttu-id="23487-118">容器登錄名。</span><span class="sxs-lookup"><span data-stu-id="23487-118">Container Registry Name.</span></span>

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

### <span data-ttu-id="23487-119">-PasswordName</span><span class="sxs-lookup"><span data-stu-id="23487-119">-PasswordName</span></span>
<span data-ttu-id="23487-120">要重新產生的密碼的名稱。</span><span class="sxs-lookup"><span data-stu-id="23487-120">The name of password to regenerate.</span></span>
<span data-ttu-id="23487-121">允許的值： password、password2。</span><span class="sxs-lookup"><span data-stu-id="23487-121">Allowed values: password, password2.</span></span>

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

### <span data-ttu-id="23487-122">-Registry</span><span class="sxs-lookup"><span data-stu-id="23487-122">-Registry</span></span>
<span data-ttu-id="23487-123">分枝 Registry 物件。</span><span class="sxs-lookup"><span data-stu-id="23487-123">Container Registry Object.</span></span>

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

### <span data-ttu-id="23487-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23487-124">-ResourceGroupName</span></span>
<span data-ttu-id="23487-125">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="23487-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="23487-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="23487-126">-ResourceId</span></span>
<span data-ttu-id="23487-127">容器登錄資源識別碼</span><span class="sxs-lookup"><span data-stu-id="23487-127">The container registry resource id</span></span>

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

### <span data-ttu-id="23487-128">-確認</span><span class="sxs-lookup"><span data-stu-id="23487-128">-Confirm</span></span>
<span data-ttu-id="23487-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="23487-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23487-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23487-130">-WhatIf</span></span>
<span data-ttu-id="23487-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="23487-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23487-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="23487-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23487-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23487-133">CommonParameters</span></span>
<span data-ttu-id="23487-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="23487-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23487-135">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="23487-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23487-136">輸入</span><span class="sxs-lookup"><span data-stu-id="23487-136">INPUTS</span></span>

### <span data-ttu-id="23487-137">PSContainerRegistry 中的 ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="23487-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

### <span data-ttu-id="23487-138">System.object</span><span class="sxs-lookup"><span data-stu-id="23487-138">System.String</span></span>

## <span data-ttu-id="23487-139">輸出</span><span class="sxs-lookup"><span data-stu-id="23487-139">OUTPUTS</span></span>

### <span data-ttu-id="23487-140">PSContainerRegistryCredential 中的 ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="23487-140">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span></span>

## <span data-ttu-id="23487-141">筆記</span><span class="sxs-lookup"><span data-stu-id="23487-141">NOTES</span></span>

## <span data-ttu-id="23487-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="23487-142">RELATED LINKS</span></span>

[<span data-ttu-id="23487-143">新-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="23487-143">New-AzContainerRegistry</span></span>](New-AzContainerRegistry.md)

[<span data-ttu-id="23487-144">更新-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="23487-144">Update-AzContainerRegistry</span></span>](Update-AzContainerRegistry.md)

[<span data-ttu-id="23487-145">AzContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="23487-145">Get-AzContainerRegistryCredential</span></span>](Get-AzContainerRegistryCredential.md)

