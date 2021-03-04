---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/update-azcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryCredential.md
ms.openlocfilehash: 71eb25c99197513bead7cb400b8a5648c137442d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902998"
---
# <span data-ttu-id="880c3-101">Update-AzContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="880c3-101">Update-AzContainerRegistryCredential</span></span>

## <span data-ttu-id="880c3-102">簡介</span><span class="sxs-lookup"><span data-stu-id="880c3-102">SYNOPSIS</span></span>
<span data-ttu-id="880c3-103">重新產生容器登錄的登入認證。</span><span class="sxs-lookup"><span data-stu-id="880c3-103">Regenerates a login credential for a container registry.</span></span>

## <span data-ttu-id="880c3-104">語法</span><span class="sxs-lookup"><span data-stu-id="880c3-104">SYNTAX</span></span>

### <span data-ttu-id="880c3-105">NameResourceGroupParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="880c3-105">NameResourceGroupParameterSet (Default)</span></span>
```
Update-AzContainerRegistryCredential [-ResourceGroupName] <String> [-Name] <String>
 -PasswordName <PasswordName> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="880c3-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="880c3-106">RegistryObjectParameterSet</span></span>
```
Update-AzContainerRegistryCredential -Registry <PSContainerRegistry> -PasswordName <PasswordName>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="880c3-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="880c3-107">ResourceIdParameterSet</span></span>
```
Update-AzContainerRegistryCredential -PasswordName <PasswordName> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="880c3-108">描述</span><span class="sxs-lookup"><span data-stu-id="880c3-108">DESCRIPTION</span></span>
<span data-ttu-id="880c3-109">此Update-AzContainerRegistryCredential Cmdlet 會重新產生容器登錄的登入認證。</span><span class="sxs-lookup"><span data-stu-id="880c3-109">The Update-AzContainerRegistryCredential cmdlet regenerates a login credential for a container registry.</span></span>

## <span data-ttu-id="880c3-110">例子</span><span class="sxs-lookup"><span data-stu-id="880c3-110">EXAMPLES</span></span>

### <span data-ttu-id="880c3-111">範例 1：重新產生容器登錄的登入認證</span><span class="sxs-lookup"><span data-stu-id="880c3-111">Example 1: Regenerate a login credential for a container registry</span></span>
```powershell
PS C:\>Update-AzContainerRegistryCredential -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -PasswordName "Password"

Username   Password                         Password2
--------   --------                         ---------
MyRegistry ++q/=K9+RH/+hwg2+3A=N+/w=J/12Ph9 //JRPkgxx+r+z/ztU=R//E==vum=pRKL
```

<span data-ttu-id="880c3-112">此命令會重新產生指定容器登錄的登入認證。</span><span class="sxs-lookup"><span data-stu-id="880c3-112">This command regenerates a login credential for the specified container registry.</span></span>
<span data-ttu-id="880c3-113">系統管理使用者必須啟用容器登錄 \` MyRegistry， \` 才能重新產生登入認證。</span><span class="sxs-lookup"><span data-stu-id="880c3-113">Admin user has to be enabled for the container registry \`MyRegistry\` to regenerate login credentials.</span></span>

## <span data-ttu-id="880c3-114">參數</span><span class="sxs-lookup"><span data-stu-id="880c3-114">PARAMETERS</span></span>

### <span data-ttu-id="880c3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="880c3-115">-DefaultProfile</span></span>
<span data-ttu-id="880c3-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="880c3-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="880c3-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="880c3-117">-Name</span></span>
<span data-ttu-id="880c3-118">容器註冊表名稱。</span><span class="sxs-lookup"><span data-stu-id="880c3-118">Container Registry Name.</span></span>

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

### <span data-ttu-id="880c3-119">-PasswordName</span><span class="sxs-lookup"><span data-stu-id="880c3-119">-PasswordName</span></span>
<span data-ttu-id="880c3-120">要重新產生的密碼名稱。</span><span class="sxs-lookup"><span data-stu-id="880c3-120">The name of password to regenerate.</span></span>
<span data-ttu-id="880c3-121">允許的值：密碼、密碼2。</span><span class="sxs-lookup"><span data-stu-id="880c3-121">Allowed values: password, password2.</span></span>

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

### <span data-ttu-id="880c3-122">-Registry</span><span class="sxs-lookup"><span data-stu-id="880c3-122">-Registry</span></span>
<span data-ttu-id="880c3-123">Container Registry 物件。</span><span class="sxs-lookup"><span data-stu-id="880c3-123">Container Registry Object.</span></span>

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

### <span data-ttu-id="880c3-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="880c3-124">-ResourceGroupName</span></span>
<span data-ttu-id="880c3-125">資源組名。</span><span class="sxs-lookup"><span data-stu-id="880c3-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="880c3-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="880c3-126">-ResourceId</span></span>
<span data-ttu-id="880c3-127">容器登錄資源識別碼</span><span class="sxs-lookup"><span data-stu-id="880c3-127">The container registry resource id</span></span>

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

### <span data-ttu-id="880c3-128">-確認</span><span class="sxs-lookup"><span data-stu-id="880c3-128">-Confirm</span></span>
<span data-ttu-id="880c3-129">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="880c3-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="880c3-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="880c3-130">-WhatIf</span></span>
<span data-ttu-id="880c3-131">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="880c3-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="880c3-132">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="880c3-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="880c3-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="880c3-133">CommonParameters</span></span>
<span data-ttu-id="880c3-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="880c3-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="880c3-135">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="880c3-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="880c3-136">輸入</span><span class="sxs-lookup"><span data-stu-id="880c3-136">INPUTS</span></span>

### <span data-ttu-id="880c3-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="880c3-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

### <span data-ttu-id="880c3-138">System.String</span><span class="sxs-lookup"><span data-stu-id="880c3-138">System.String</span></span>

## <span data-ttu-id="880c3-139">輸出</span><span class="sxs-lookup"><span data-stu-id="880c3-139">OUTPUTS</span></span>

### <span data-ttu-id="880c3-140">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="880c3-140">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span></span>

## <span data-ttu-id="880c3-141">筆記</span><span class="sxs-lookup"><span data-stu-id="880c3-141">NOTES</span></span>

## <span data-ttu-id="880c3-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="880c3-142">RELATED LINKS</span></span>

[<span data-ttu-id="880c3-143">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="880c3-143">New-AzContainerRegistry</span></span>](New-AzContainerRegistry.md)

[<span data-ttu-id="880c3-144">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="880c3-144">Update-AzContainerRegistry</span></span>](Update-AzContainerRegistry.md)

[<span data-ttu-id="880c3-145">Get-AzContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="880c3-145">Get-AzContainerRegistryCredential</span></span>](Get-AzContainerRegistryCredential.md)

