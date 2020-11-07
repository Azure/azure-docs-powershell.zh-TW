---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/new-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/New-AzureRmContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/New-AzureRmContainerRegistry.md
ms.openlocfilehash: b70e4b4c184cfb6ebc5473cb0f49dec712bc62fd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623422"
---
# <span data-ttu-id="f7165-101">New-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="f7165-101">New-AzureRmContainerRegistry</span></span>

## <span data-ttu-id="f7165-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f7165-102">SYNOPSIS</span></span>
<span data-ttu-id="f7165-103">建立容器註冊。</span><span class="sxs-lookup"><span data-stu-id="f7165-103">Creates a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f7165-104">句法</span><span class="sxs-lookup"><span data-stu-id="f7165-104">SYNTAX</span></span>

```
New-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-Sku] <String>
 [-Location <String>] [-EnableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7165-105">說明</span><span class="sxs-lookup"><span data-stu-id="f7165-105">DESCRIPTION</span></span>
<span data-ttu-id="f7165-106">New-AzureRmContainerRegistry Cmdlet 會建立容器註冊。</span><span class="sxs-lookup"><span data-stu-id="f7165-106">The New-AzureRmContainerRegistry cmdlet creates a container registry.</span></span>

## <span data-ttu-id="f7165-107">示例</span><span class="sxs-lookup"><span data-stu-id="f7165-107">EXAMPLES</span></span>

### <span data-ttu-id="f7165-108">範例1：使用新的儲存空間帳戶建立容器註冊表。</span><span class="sxs-lookup"><span data-stu-id="f7165-108">Example 1: Create a container registry with a new storage account.</span></span>
```powershell
PS C:\>New-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic"

   Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="f7165-109">這個命令會在 [資源群組 MyResourceGroup] 中使用新的儲存空間帳戶來建立容器註冊表 \` \` 。</span><span class="sxs-lookup"><span data-stu-id="f7165-109">This command creates a container registry with a new storage account in the resource group \`MyResourceGroup\`.</span></span>

### <span data-ttu-id="f7165-110">範例2：在已啟用系統管理員使用者的情況中建立容器註冊表。</span><span class="sxs-lookup"><span data-stu-id="f7165-110">Example 2: Create a container registry with admin user enabled.</span></span>
```powershell
PS C:\>New-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic" -EnableAdminUser

  Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="f7165-111">這個命令會在啟用系統管理員使用者的情況下建立容器註冊表。</span><span class="sxs-lookup"><span data-stu-id="f7165-111">This command creates a container registry with admin user enabled.</span></span>

### <span data-ttu-id="f7165-112">範例3：使用現有的儲存空間帳戶建立容器註冊。</span><span class="sxs-lookup"><span data-stu-id="f7165-112">Example 3: Create a container registry with an existing storage account.</span></span>
```powershell
PS C:\>New-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic" -StorageAccountName "mystorageaccount"

  Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="f7165-113">這個命令會 \` \` 在同一個訂閱中使用現有的儲存空間帳戶 mystorageaccount 來建立容器註冊表。</span><span class="sxs-lookup"><span data-stu-id="f7165-113">This command creates a container registry with an existing storage account \`mystorageaccount\` in the same subscription.</span></span>

## <span data-ttu-id="f7165-114">參數</span><span class="sxs-lookup"><span data-stu-id="f7165-114">PARAMETERS</span></span>

### <span data-ttu-id="f7165-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7165-115">-DefaultProfile</span></span>
<span data-ttu-id="f7165-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="f7165-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f7165-117">-EnableAdminUser</span><span class="sxs-lookup"><span data-stu-id="f7165-117">-EnableAdminUser</span></span>
<span data-ttu-id="f7165-118">針對容器登錄啟用 [管理員使用者]。</span><span class="sxs-lookup"><span data-stu-id="f7165-118">Enable admin user for the container registry.</span></span>

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

### <span data-ttu-id="f7165-119">-位置</span><span class="sxs-lookup"><span data-stu-id="f7165-119">-Location</span></span>
<span data-ttu-id="f7165-120">容器登錄位置。</span><span class="sxs-lookup"><span data-stu-id="f7165-120">Container Registry Location.</span></span>
<span data-ttu-id="f7165-121">預設為資源群組的位置。</span><span class="sxs-lookup"><span data-stu-id="f7165-121">Default to the location of the resource group.</span></span>

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

### <span data-ttu-id="f7165-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="f7165-122">-Name</span></span>
<span data-ttu-id="f7165-123">容器登錄名。</span><span class="sxs-lookup"><span data-stu-id="f7165-123">Container Registry Name.</span></span>

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

### <span data-ttu-id="f7165-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7165-124">-ResourceGroupName</span></span>
<span data-ttu-id="f7165-125">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="f7165-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="f7165-126">-Sku</span><span class="sxs-lookup"><span data-stu-id="f7165-126">-Sku</span></span>
<span data-ttu-id="f7165-127">容器註冊 SKU。</span><span class="sxs-lookup"><span data-stu-id="f7165-127">Container Registry SKU.</span></span>
<span data-ttu-id="f7165-128">允許的值：基本。</span><span class="sxs-lookup"><span data-stu-id="f7165-128">Allowed values: Basic.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ContainerRegistrySku, RegistrySku
Accepted values: Classic, Basic, Premium, Standard

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7165-129">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="f7165-129">-StorageAccountName</span></span>
<span data-ttu-id="f7165-130">現有儲存空間帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="f7165-130">The name of an existing storage account.</span></span>

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

### <span data-ttu-id="f7165-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="f7165-131">-Tag</span></span>
<span data-ttu-id="f7165-132">以雜湊資料表形式顯示的索引鍵值對。</span><span class="sxs-lookup"><span data-stu-id="f7165-132">Container Registry Tags.Key-value pairs in the form of a hash table.</span></span>
<span data-ttu-id="f7165-133">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="f7165-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="f7165-134">-確認</span><span class="sxs-lookup"><span data-stu-id="f7165-134">-Confirm</span></span>
<span data-ttu-id="f7165-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f7165-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7165-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7165-136">-WhatIf</span></span>
<span data-ttu-id="f7165-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f7165-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7165-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f7165-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7165-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7165-139">CommonParameters</span></span>
<span data-ttu-id="f7165-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f7165-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7165-141">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f7165-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7165-142">輸入</span><span class="sxs-lookup"><span data-stu-id="f7165-142">INPUTS</span></span>

### <span data-ttu-id="f7165-143">System.object</span><span class="sxs-lookup"><span data-stu-id="f7165-143">System.String</span></span>

## <span data-ttu-id="f7165-144">輸出</span><span class="sxs-lookup"><span data-stu-id="f7165-144">OUTPUTS</span></span>

### <span data-ttu-id="f7165-145">PSContainerRegistry 中的 ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="f7165-145">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="f7165-146">筆記</span><span class="sxs-lookup"><span data-stu-id="f7165-146">NOTES</span></span>

## <span data-ttu-id="f7165-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="f7165-147">RELATED LINKS</span></span>

[<span data-ttu-id="f7165-148">AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="f7165-148">Get-AzureRmContainerRegistry</span></span>](Get-AzureRmContainerRegistry.md)

[<span data-ttu-id="f7165-149">更新-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="f7165-149">Update-AzureRmContainerRegistry</span></span>](Update-AzureRmContainerRegistry.md)

[<span data-ttu-id="f7165-150">移除-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="f7165-150">Remove-AzureRmContainerRegistry</span></span>](Remove-AzureRmContainerRegistry.md)

