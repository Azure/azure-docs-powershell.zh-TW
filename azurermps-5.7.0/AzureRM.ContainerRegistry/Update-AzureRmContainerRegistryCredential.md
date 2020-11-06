---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/update-azurermcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistryCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistryCredential.md
ms.openlocfilehash: 46eb802b4a91aa7ee7d370ed9ca93805497f21d1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449920"
---
# <span data-ttu-id="8a47e-101">Update-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="8a47e-101">Update-AzureRmContainerRegistryCredential</span></span>

## <span data-ttu-id="8a47e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8a47e-102">SYNOPSIS</span></span>
<span data-ttu-id="8a47e-103">重新產生容器註冊的登入認證。</span><span class="sxs-lookup"><span data-stu-id="8a47e-103">Regenerates a login credential for a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8a47e-104">句法</span><span class="sxs-lookup"><span data-stu-id="8a47e-104">SYNTAX</span></span>

### <span data-ttu-id="8a47e-105">NameResourceGroupParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="8a47e-105">NameResourceGroupParameterSet (Default)</span></span>
```
Update-AzureRmContainerRegistryCredential [-ResourceGroupName] <String> [-Name] <String>
 -PasswordName <PasswordName> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8a47e-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8a47e-106">RegistryObjectParameterSet</span></span>
```
Update-AzureRmContainerRegistryCredential -Registry <PSContainerRegistry> -PasswordName <PasswordName>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a47e-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8a47e-107">ResourceIdParameterSet</span></span>
```
Update-AzureRmContainerRegistryCredential -PasswordName <PasswordName> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8a47e-108">說明</span><span class="sxs-lookup"><span data-stu-id="8a47e-108">DESCRIPTION</span></span>
<span data-ttu-id="8a47e-109">Update-AzureRmContainerRegistryCredential Cmdlet 會為容器註冊重新產生登入認證。</span><span class="sxs-lookup"><span data-stu-id="8a47e-109">The Update-AzureRmContainerRegistryCredential cmdlet regenerates a login credential for a container registry.</span></span>

## <span data-ttu-id="8a47e-110">示例</span><span class="sxs-lookup"><span data-stu-id="8a47e-110">EXAMPLES</span></span>

### <span data-ttu-id="8a47e-111">範例1：為容器註冊表重新產生登入認證</span><span class="sxs-lookup"><span data-stu-id="8a47e-111">Example 1: Regenerate a login credential for a container registry</span></span>
```powershell
PS C:\>Update-AzureRmContainerRegistryCredential -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -PasswordName "Password"

Username   Password                         Password2
--------   --------                         ---------
MyRegistry ++q/=K9+RH/+hwg2+3A=N+/w=J/12Ph9 //JRPkgxx+r+z/ztU=R//E==vum=pRKL
```

<span data-ttu-id="8a47e-112">這個命令會為指定的容器註冊表重新產生登入認證。</span><span class="sxs-lookup"><span data-stu-id="8a47e-112">This command regenerates a login credential for the specified container registry.</span></span>
<span data-ttu-id="8a47e-113">管理員使用者必須啟用容器 \` \` 登錄 MyRegistry，才能重新產生登入認證。</span><span class="sxs-lookup"><span data-stu-id="8a47e-113">Admin user has to be enabled for the container registry \`MyRegistry\` to regenerate login credentials.</span></span>

## <span data-ttu-id="8a47e-114">參數</span><span class="sxs-lookup"><span data-stu-id="8a47e-114">PARAMETERS</span></span>

### <span data-ttu-id="8a47e-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="8a47e-115">-Name</span></span>
<span data-ttu-id="8a47e-116">容器登錄名。</span><span class="sxs-lookup"><span data-stu-id="8a47e-116">Container Registry Name.</span></span>

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

### <span data-ttu-id="8a47e-117">-PasswordName</span><span class="sxs-lookup"><span data-stu-id="8a47e-117">-PasswordName</span></span>
<span data-ttu-id="8a47e-118">要重新產生的密碼的名稱。</span><span class="sxs-lookup"><span data-stu-id="8a47e-118">The name of password to regenerate.</span></span>
<span data-ttu-id="8a47e-119">允許的值： password、password2。</span><span class="sxs-lookup"><span data-stu-id="8a47e-119">Allowed values: password, password2.</span></span>

```yaml
Type: PasswordName
Parameter Sets: (All)
Aliases: 
Accepted values: Password, Password2

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a47e-120">-Registry</span><span class="sxs-lookup"><span data-stu-id="8a47e-120">-Registry</span></span>
<span data-ttu-id="8a47e-121">分枝 Registry 物件。</span><span class="sxs-lookup"><span data-stu-id="8a47e-121">Container Registry Object.</span></span>

```yaml
Type: PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8a47e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a47e-122">-ResourceGroupName</span></span>
<span data-ttu-id="8a47e-123">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="8a47e-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="8a47e-124">-確認</span><span class="sxs-lookup"><span data-stu-id="8a47e-124">-Confirm</span></span>
<span data-ttu-id="8a47e-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8a47e-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a47e-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a47e-126">-WhatIf</span></span>
<span data-ttu-id="8a47e-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8a47e-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a47e-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8a47e-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a47e-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a47e-129">-DefaultProfile</span></span>
<span data-ttu-id="8a47e-130">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="8a47e-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8a47e-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8a47e-131">-ResourceId</span></span>
<span data-ttu-id="8a47e-132">容器登錄資源識別碼</span><span class="sxs-lookup"><span data-stu-id="8a47e-132">The container registry resource id</span></span>

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

### <span data-ttu-id="8a47e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a47e-133">CommonParameters</span></span>
<span data-ttu-id="8a47e-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8a47e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a47e-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8a47e-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a47e-136">輸入</span><span class="sxs-lookup"><span data-stu-id="8a47e-136">INPUTS</span></span>

### <span data-ttu-id="8a47e-137">PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="8a47e-137">PSContainerRegistry</span></span>
<span data-ttu-id="8a47e-138">參數 "Registry" 接受管線中 "PSContainerRegistry" 類型的值</span><span class="sxs-lookup"><span data-stu-id="8a47e-138">Parameter 'Registry' accepts value of type 'PSContainerRegistry' from the pipeline</span></span>

## <span data-ttu-id="8a47e-139">輸出</span><span class="sxs-lookup"><span data-stu-id="8a47e-139">OUTPUTS</span></span>

### <span data-ttu-id="8a47e-140">PSContainerRegistryCredential 中的 ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="8a47e-140">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span></span>

## <span data-ttu-id="8a47e-141">筆記</span><span class="sxs-lookup"><span data-stu-id="8a47e-141">NOTES</span></span>

## <span data-ttu-id="8a47e-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="8a47e-142">RELATED LINKS</span></span>

[<span data-ttu-id="8a47e-143">新-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="8a47e-143">New-AzureRmContainerRegistry</span></span>](New-AzureRmContainerRegistry.md)

[<span data-ttu-id="8a47e-144">更新-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="8a47e-144">Update-AzureRmContainerRegistry</span></span>](Update-AzureRmContainerRegistry.md)

[<span data-ttu-id="8a47e-145">AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="8a47e-145">Get-AzureRmContainerRegistryCredential</span></span>](Get-AzureRmContainerRegistryCredential.md)

