---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/new-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistry.md
ms.openlocfilehash: 4d9b788637e0c97d8f129df33ac7e4050ce916d7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904718"
---
# <span data-ttu-id="98cc0-101">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="98cc0-101">New-AzContainerRegistry</span></span>

## <span data-ttu-id="98cc0-102">簡介</span><span class="sxs-lookup"><span data-stu-id="98cc0-102">SYNOPSIS</span></span>
<span data-ttu-id="98cc0-103">建立容器註冊表。</span><span class="sxs-lookup"><span data-stu-id="98cc0-103">Creates a container registry.</span></span>

## <span data-ttu-id="98cc0-104">語法</span><span class="sxs-lookup"><span data-stu-id="98cc0-104">SYNTAX</span></span>

```
New-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-Sku] <String> [-Location <String>]
 [-EnableAdminUser] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="98cc0-105">描述</span><span class="sxs-lookup"><span data-stu-id="98cc0-105">DESCRIPTION</span></span>
<span data-ttu-id="98cc0-106">Cmdlet New-AzContainerRegistry建立容器註冊表。</span><span class="sxs-lookup"><span data-stu-id="98cc0-106">The New-AzContainerRegistry cmdlet creates a container registry.</span></span>

## <span data-ttu-id="98cc0-107">例子</span><span class="sxs-lookup"><span data-stu-id="98cc0-107">EXAMPLES</span></span>

### <span data-ttu-id="98cc0-108">範例 1：使用新的儲存帳戶建立容器登錄。</span><span class="sxs-lookup"><span data-stu-id="98cc0-108">Example 1: Create a container registry with a new storage account.</span></span>
```powershell
PS C:\>New-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic"

   Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="98cc0-109">此命令會使用資源群組 MyResourceGroup 中的新儲存帳戶建立 \` 容器登錄 \` 。</span><span class="sxs-lookup"><span data-stu-id="98cc0-109">This command creates a container registry with a new storage account in the resource group \`MyResourceGroup\`.</span></span>

### <span data-ttu-id="98cc0-110">範例 2：建立啟用系統管理員使用者的容器登錄。</span><span class="sxs-lookup"><span data-stu-id="98cc0-110">Example 2: Create a container registry with admin user enabled.</span></span>
```powershell
PS C:\>New-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic" -EnableAdminUser

  Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="98cc0-111">此命令會建立啟用系統管理員使用者的容器登錄。</span><span class="sxs-lookup"><span data-stu-id="98cc0-111">This command creates a container registry with admin user enabled.</span></span>

## <span data-ttu-id="98cc0-112">參數</span><span class="sxs-lookup"><span data-stu-id="98cc0-112">PARAMETERS</span></span>

### <span data-ttu-id="98cc0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98cc0-113">-DefaultProfile</span></span>
<span data-ttu-id="98cc0-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="98cc0-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="98cc0-115">-EnableAdminUser</span><span class="sxs-lookup"><span data-stu-id="98cc0-115">-EnableAdminUser</span></span>
<span data-ttu-id="98cc0-116">啟用容器登錄的系統管理員使用者。</span><span class="sxs-lookup"><span data-stu-id="98cc0-116">Enable admin user for the container registry.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: EnableAdmin

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98cc0-117">-位置</span><span class="sxs-lookup"><span data-stu-id="98cc0-117">-Location</span></span>
<span data-ttu-id="98cc0-118">容器註冊表位置。</span><span class="sxs-lookup"><span data-stu-id="98cc0-118">Container Registry Location.</span></span>
<span data-ttu-id="98cc0-119">預設為資源群組的位置。</span><span class="sxs-lookup"><span data-stu-id="98cc0-119">Default to the location of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98cc0-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="98cc0-120">-Name</span></span>
<span data-ttu-id="98cc0-121">容器註冊表名稱。</span><span class="sxs-lookup"><span data-stu-id="98cc0-121">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98cc0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98cc0-122">-ResourceGroupName</span></span>
<span data-ttu-id="98cc0-123">資源組名。</span><span class="sxs-lookup"><span data-stu-id="98cc0-123">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98cc0-124">-SKU</span><span class="sxs-lookup"><span data-stu-id="98cc0-124">-Sku</span></span>
<span data-ttu-id="98cc0-125">Container Registry SKU.</span><span class="sxs-lookup"><span data-stu-id="98cc0-125">Container Registry SKU.</span></span>
<span data-ttu-id="98cc0-126">允許的值：基本。</span><span class="sxs-lookup"><span data-stu-id="98cc0-126">Allowed values: Basic.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ContainerRegistrySku, RegistrySku
Accepted values: Basic, Premium, Standard

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98cc0-127">-標記</span><span class="sxs-lookup"><span data-stu-id="98cc0-127">-Tag</span></span>
<span data-ttu-id="98cc0-128">Container Registry Tags.Key-value pairs in the form of a hash table.</span><span class="sxs-lookup"><span data-stu-id="98cc0-128">Container Registry Tags.Key-value pairs in the form of a hash table.</span></span>
<span data-ttu-id="98cc0-129">例如：@{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="98cc0-129">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98cc0-130">-確認</span><span class="sxs-lookup"><span data-stu-id="98cc0-130">-Confirm</span></span>
<span data-ttu-id="98cc0-131">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="98cc0-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98cc0-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98cc0-132">-WhatIf</span></span>
<span data-ttu-id="98cc0-133">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="98cc0-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98cc0-134">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="98cc0-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98cc0-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98cc0-135">CommonParameters</span></span>
<span data-ttu-id="98cc0-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="98cc0-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98cc0-137">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="98cc0-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98cc0-138">輸入</span><span class="sxs-lookup"><span data-stu-id="98cc0-138">INPUTS</span></span>

### <span data-ttu-id="98cc0-139">System.String</span><span class="sxs-lookup"><span data-stu-id="98cc0-139">System.String</span></span>

## <span data-ttu-id="98cc0-140">輸出</span><span class="sxs-lookup"><span data-stu-id="98cc0-140">OUTPUTS</span></span>

### <span data-ttu-id="98cc0-141">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="98cc0-141">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="98cc0-142">筆記</span><span class="sxs-lookup"><span data-stu-id="98cc0-142">NOTES</span></span>

## <span data-ttu-id="98cc0-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="98cc0-143">RELATED LINKS</span></span>

[<span data-ttu-id="98cc0-144">Get-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="98cc0-144">Get-AzContainerRegistry</span></span>](Get-AzContainerRegistry.md)

[<span data-ttu-id="98cc0-145">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="98cc0-145">Update-AzContainerRegistry</span></span>](Update-AzContainerRegistry.md)

[<span data-ttu-id="98cc0-146">Remove-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="98cc0-146">Remove-AzContainerRegistry</span></span>](Remove-AzContainerRegistry.md)

