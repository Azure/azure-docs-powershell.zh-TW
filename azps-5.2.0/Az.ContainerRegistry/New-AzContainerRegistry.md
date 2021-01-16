---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/new-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistry.md
ms.openlocfilehash: 0f1e95c97076c13ed74c1ee708577a2429bcb979
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98280356"
---
# <span data-ttu-id="e35db-101">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="e35db-101">New-AzContainerRegistry</span></span>

## <span data-ttu-id="e35db-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e35db-102">SYNOPSIS</span></span>
<span data-ttu-id="e35db-103">建立容器註冊。</span><span class="sxs-lookup"><span data-stu-id="e35db-103">Creates a container registry.</span></span>

## <span data-ttu-id="e35db-104">句法</span><span class="sxs-lookup"><span data-stu-id="e35db-104">SYNTAX</span></span>

```
New-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-Sku] <String> [-Location <String>]
 [-EnableAdminUser] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e35db-105">說明</span><span class="sxs-lookup"><span data-stu-id="e35db-105">DESCRIPTION</span></span>
<span data-ttu-id="e35db-106">New-AzContainerRegistry Cmdlet 會建立容器註冊。</span><span class="sxs-lookup"><span data-stu-id="e35db-106">The New-AzContainerRegistry cmdlet creates a container registry.</span></span>

## <span data-ttu-id="e35db-107">示例</span><span class="sxs-lookup"><span data-stu-id="e35db-107">EXAMPLES</span></span>

### <span data-ttu-id="e35db-108">範例1：使用新的儲存空間帳戶建立容器註冊表。</span><span class="sxs-lookup"><span data-stu-id="e35db-108">Example 1: Create a container registry with a new storage account.</span></span>
```powershell
PS C:\>New-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic"

   Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="e35db-109">這個命令會在 [資源群組 MyResourceGroup] 中使用新的儲存空間帳戶來建立容器註冊表 \` \` 。</span><span class="sxs-lookup"><span data-stu-id="e35db-109">This command creates a container registry with a new storage account in the resource group \`MyResourceGroup\`.</span></span>

### <span data-ttu-id="e35db-110">範例2：在已啟用系統管理員使用者的情況中建立容器註冊表。</span><span class="sxs-lookup"><span data-stu-id="e35db-110">Example 2: Create a container registry with admin user enabled.</span></span>
```powershell
PS C:\>New-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic" -EnableAdminUser

  Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="e35db-111">這個命令會在啟用系統管理員使用者的情況下建立容器註冊表。</span><span class="sxs-lookup"><span data-stu-id="e35db-111">This command creates a container registry with admin user enabled.</span></span>

## <span data-ttu-id="e35db-112">參數</span><span class="sxs-lookup"><span data-stu-id="e35db-112">PARAMETERS</span></span>

### <span data-ttu-id="e35db-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e35db-113">-DefaultProfile</span></span>
<span data-ttu-id="e35db-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="e35db-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e35db-115">-EnableAdminUser</span><span class="sxs-lookup"><span data-stu-id="e35db-115">-EnableAdminUser</span></span>
<span data-ttu-id="e35db-116">針對容器登錄啟用 [管理員使用者]。</span><span class="sxs-lookup"><span data-stu-id="e35db-116">Enable admin user for the container registry.</span></span>

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

### <span data-ttu-id="e35db-117">-位置</span><span class="sxs-lookup"><span data-stu-id="e35db-117">-Location</span></span>
<span data-ttu-id="e35db-118">容器登錄位置。</span><span class="sxs-lookup"><span data-stu-id="e35db-118">Container Registry Location.</span></span>
<span data-ttu-id="e35db-119">預設為資源群組的位置。</span><span class="sxs-lookup"><span data-stu-id="e35db-119">Default to the location of the resource group.</span></span>

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

### <span data-ttu-id="e35db-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="e35db-120">-Name</span></span>
<span data-ttu-id="e35db-121">容器登錄名。</span><span class="sxs-lookup"><span data-stu-id="e35db-121">Container Registry Name.</span></span>

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

### <span data-ttu-id="e35db-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e35db-122">-ResourceGroupName</span></span>
<span data-ttu-id="e35db-123">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="e35db-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="e35db-124">-Sku</span><span class="sxs-lookup"><span data-stu-id="e35db-124">-Sku</span></span>
<span data-ttu-id="e35db-125">容器註冊 SKU。</span><span class="sxs-lookup"><span data-stu-id="e35db-125">Container Registry SKU.</span></span>
<span data-ttu-id="e35db-126">允許的值：基本。</span><span class="sxs-lookup"><span data-stu-id="e35db-126">Allowed values: Basic.</span></span>

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

### <span data-ttu-id="e35db-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="e35db-127">-Tag</span></span>
<span data-ttu-id="e35db-128">以雜湊資料表形式顯示的索引鍵值對。</span><span class="sxs-lookup"><span data-stu-id="e35db-128">Container Registry Tags.Key-value pairs in the form of a hash table.</span></span>
<span data-ttu-id="e35db-129">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="e35db-129">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="e35db-130">-確認</span><span class="sxs-lookup"><span data-stu-id="e35db-130">-Confirm</span></span>
<span data-ttu-id="e35db-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e35db-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e35db-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e35db-132">-WhatIf</span></span>
<span data-ttu-id="e35db-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e35db-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e35db-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e35db-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e35db-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e35db-135">CommonParameters</span></span>
<span data-ttu-id="e35db-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e35db-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e35db-137">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e35db-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e35db-138">輸入</span><span class="sxs-lookup"><span data-stu-id="e35db-138">INPUTS</span></span>

### <span data-ttu-id="e35db-139">System.object</span><span class="sxs-lookup"><span data-stu-id="e35db-139">System.String</span></span>

## <span data-ttu-id="e35db-140">輸出</span><span class="sxs-lookup"><span data-stu-id="e35db-140">OUTPUTS</span></span>

### <span data-ttu-id="e35db-141">PSContainerRegistry 中的 ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="e35db-141">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="e35db-142">筆記</span><span class="sxs-lookup"><span data-stu-id="e35db-142">NOTES</span></span>

## <span data-ttu-id="e35db-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="e35db-143">RELATED LINKS</span></span>

[<span data-ttu-id="e35db-144">AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="e35db-144">Get-AzContainerRegistry</span></span>](Get-AzContainerRegistry.md)

[<span data-ttu-id="e35db-145">更新-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="e35db-145">Update-AzContainerRegistry</span></span>](Update-AzContainerRegistry.md)

[<span data-ttu-id="e35db-146">移除-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="e35db-146">Remove-AzContainerRegistry</span></span>](Remove-AzContainerRegistry.md)

