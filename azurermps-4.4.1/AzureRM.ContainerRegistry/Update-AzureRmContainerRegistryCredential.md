---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistryCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistryCredential.md
ms.openlocfilehash: e65367a94e946aee83df2087463bd0081e925862
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624153"
---
# <span data-ttu-id="842eb-101">Update-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="842eb-101">Update-AzureRmContainerRegistryCredential</span></span>

## <span data-ttu-id="842eb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="842eb-102">SYNOPSIS</span></span>
<span data-ttu-id="842eb-103">重新產生容器註冊的登入認證。</span><span class="sxs-lookup"><span data-stu-id="842eb-103">Regenerates a login credential for a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="842eb-104">句法</span><span class="sxs-lookup"><span data-stu-id="842eb-104">SYNTAX</span></span>

### <span data-ttu-id="842eb-105">NameResourceGroupParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="842eb-105">NameResourceGroupParameterSet (Default)</span></span>
```
Update-AzureRmContainerRegistryCredential [-ResourceGroupName] <String> [-Name] <String>
 -PasswordName <PasswordName> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="842eb-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="842eb-106">RegistryObjectParameterSet</span></span>
```
Update-AzureRmContainerRegistryCredential -Registry <PSContainerRegistry> -PasswordName <PasswordName>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="842eb-107">說明</span><span class="sxs-lookup"><span data-stu-id="842eb-107">DESCRIPTION</span></span>
<span data-ttu-id="842eb-108">**AzureRmContainerRegistryCredential** Cmdlet 會為容器註冊重新產生登入認證。</span><span class="sxs-lookup"><span data-stu-id="842eb-108">The **Update-AzureRmContainerRegistryCredential** cmdlet regenerates a login credential for a container registry.</span></span>

## <span data-ttu-id="842eb-109">示例</span><span class="sxs-lookup"><span data-stu-id="842eb-109">EXAMPLES</span></span>

### <span data-ttu-id="842eb-110">範例1：為容器註冊表重新產生登入認證</span><span class="sxs-lookup"><span data-stu-id="842eb-110">Example 1: Regenerate a login credential for a container registry</span></span>
```
PS C:\>Update-AzureRmContainerRegistryCredential -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -PasswordName "Password"

Username   Password                         Password2
--------   --------                         ---------
MyRegistry ++q/=K9+RH/+hwg2+3A=N+/w=J/12Ph9 //JRPkgxx+r+z/ztU=R//E==vum=pRKL
```

<span data-ttu-id="842eb-111">這個命令會為指定的容器註冊表重新產生登入認證。</span><span class="sxs-lookup"><span data-stu-id="842eb-111">This command regenerates a login credential for the specified container registry.</span></span> <span data-ttu-id="842eb-112">管理員使用者必須啟用容器 `MyRegistry` 登錄，才能重新產生登入認證。</span><span class="sxs-lookup"><span data-stu-id="842eb-112">Admin user has to be enabled for the container registry `MyRegistry` to regenerate login credentials.</span></span>

## <span data-ttu-id="842eb-113">參數</span><span class="sxs-lookup"><span data-stu-id="842eb-113">PARAMETERS</span></span>

### <span data-ttu-id="842eb-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="842eb-114">-Name</span></span>
<span data-ttu-id="842eb-115">容器登錄名。</span><span class="sxs-lookup"><span data-stu-id="842eb-115">Container Registry Name.</span></span>

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

### <span data-ttu-id="842eb-116">-PasswordName</span><span class="sxs-lookup"><span data-stu-id="842eb-116">-PasswordName</span></span>
<span data-ttu-id="842eb-117">要重新產生的密碼的名稱。</span><span class="sxs-lookup"><span data-stu-id="842eb-117">The name of password to regenerate.</span></span>
<span data-ttu-id="842eb-118">允許的值： password、password2。</span><span class="sxs-lookup"><span data-stu-id="842eb-118">Allowed values: password, password2.</span></span>

```yaml
Type: Microsoft.Azure.Management.ContainerRegistry.Models.PasswordName
Parameter Sets: (All)
Aliases: 
Accepted values: Password, Password2

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="842eb-119">-Registry</span><span class="sxs-lookup"><span data-stu-id="842eb-119">-Registry</span></span>
<span data-ttu-id="842eb-120">分枝 Registry 物件。</span><span class="sxs-lookup"><span data-stu-id="842eb-120">Container Registry Object.</span></span>

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

### <span data-ttu-id="842eb-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="842eb-121">-ResourceGroupName</span></span>
<span data-ttu-id="842eb-122">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="842eb-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="842eb-123">-確認</span><span class="sxs-lookup"><span data-stu-id="842eb-123">-Confirm</span></span>
<span data-ttu-id="842eb-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="842eb-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="842eb-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="842eb-125">-WhatIf</span></span>
<span data-ttu-id="842eb-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="842eb-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="842eb-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="842eb-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="842eb-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="842eb-128">-DefaultProfile</span></span>
<span data-ttu-id="842eb-129">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="842eb-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="842eb-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="842eb-130">CommonParameters</span></span>
<span data-ttu-id="842eb-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="842eb-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="842eb-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="842eb-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="842eb-133">輸入</span><span class="sxs-lookup"><span data-stu-id="842eb-133">INPUTS</span></span>

### <span data-ttu-id="842eb-134">PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="842eb-134">PSContainerRegistry</span></span>
<span data-ttu-id="842eb-135">參數 "Registry" 接受管線中 "PSContainerRegistry" 類型的值</span><span class="sxs-lookup"><span data-stu-id="842eb-135">Parameter 'Registry' accepts value of type 'PSContainerRegistry' from the pipeline</span></span>

## <span data-ttu-id="842eb-136">輸出</span><span class="sxs-lookup"><span data-stu-id="842eb-136">OUTPUTS</span></span>

### <span data-ttu-id="842eb-137">PSContainerRegistryCredential 中的 ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="842eb-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span></span>

## <span data-ttu-id="842eb-138">筆記</span><span class="sxs-lookup"><span data-stu-id="842eb-138">NOTES</span></span>

## <span data-ttu-id="842eb-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="842eb-139">RELATED LINKS</span></span>

[<span data-ttu-id="842eb-140">新-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="842eb-140">New-AzureRmContainerRegistry</span></span>](./New-AzureRmContainerRegistry.md)

[<span data-ttu-id="842eb-141">更新-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="842eb-141">Update-AzureRmContainerRegistry</span></span>](./Update-AzureRmContainerRegistry.md)

[<span data-ttu-id="842eb-142">AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="842eb-142">Get-AzureRmContainerRegistryCredential</span></span>](./Get-AzureRmContainerRegistryCredential.md)

