---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/new-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/New-AzureRmContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/New-AzureRmContainerRegistry.md
ms.openlocfilehash: ce72af78fec87182e1061259cd0c0d51d9819767
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446323"
---
# <span data-ttu-id="31004-101">New-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="31004-101">New-AzureRmContainerRegistry</span></span>

## <span data-ttu-id="31004-102">摘要</span><span class="sxs-lookup"><span data-stu-id="31004-102">SYNOPSIS</span></span>
<span data-ttu-id="31004-103">建立容器註冊。</span><span class="sxs-lookup"><span data-stu-id="31004-103">Creates a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="31004-104">句法</span><span class="sxs-lookup"><span data-stu-id="31004-104">SYNTAX</span></span>

```
New-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-Sku] <String>
 [-Location <String>] [-EnableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="31004-105">說明</span><span class="sxs-lookup"><span data-stu-id="31004-105">DESCRIPTION</span></span>
<span data-ttu-id="31004-106">New-AzureRmContainerRegistry Cmdlet 會建立容器註冊。</span><span class="sxs-lookup"><span data-stu-id="31004-106">The New-AzureRmContainerRegistry cmdlet creates a container registry.</span></span>

## <span data-ttu-id="31004-107">示例</span><span class="sxs-lookup"><span data-stu-id="31004-107">EXAMPLES</span></span>

### <span data-ttu-id="31004-108">範例1：使用新的儲存空間帳戶建立容器註冊表。</span><span class="sxs-lookup"><span data-stu-id="31004-108">Example 1: Create a container registry with a new storage account.</span></span>
```powershell
PS C:\>New-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic"

   Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="31004-109">這個命令會在 [資源群組 MyResourceGroup] 中使用新的儲存空間帳戶來建立容器註冊表 \` \` 。</span><span class="sxs-lookup"><span data-stu-id="31004-109">This command creates a container registry with a new storage account in the resource group \`MyResourceGroup\`.</span></span>

### <span data-ttu-id="31004-110">範例2：在已啟用系統管理員使用者的情況中建立容器註冊表。</span><span class="sxs-lookup"><span data-stu-id="31004-110">Example 2: Create a container registry with admin user enabled.</span></span>
```powershell
PS C:\>New-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic" -EnableAdminUser

  Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="31004-111">這個命令會在啟用系統管理員使用者的情況下建立容器註冊表。</span><span class="sxs-lookup"><span data-stu-id="31004-111">This command creates a container registry with admin user enabled.</span></span>

### <span data-ttu-id="31004-112">範例3：使用現有的儲存空間帳戶建立容器註冊。</span><span class="sxs-lookup"><span data-stu-id="31004-112">Example 3: Create a container registry with an existing storage account.</span></span>
```powershell
PS C:\>New-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic" -StorageAccountName "mystorageaccount"

  Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="31004-113">這個命令會 \` \` 在同一個訂閱中使用現有的儲存空間帳戶 mystorageaccount 來建立容器註冊表。</span><span class="sxs-lookup"><span data-stu-id="31004-113">This command creates a container registry with an existing storage account \`mystorageaccount\` in the same subscription.</span></span>

## <span data-ttu-id="31004-114">參數</span><span class="sxs-lookup"><span data-stu-id="31004-114">PARAMETERS</span></span>

### <span data-ttu-id="31004-115">-EnableAdminUser</span><span class="sxs-lookup"><span data-stu-id="31004-115">-EnableAdminUser</span></span>
<span data-ttu-id="31004-116">針對容器登錄啟用 [管理員使用者]。</span><span class="sxs-lookup"><span data-stu-id="31004-116">Enable admin user for the container registry.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: EnableAdmin

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31004-117">-位置</span><span class="sxs-lookup"><span data-stu-id="31004-117">-Location</span></span>
<span data-ttu-id="31004-118">容器登錄位置。</span><span class="sxs-lookup"><span data-stu-id="31004-118">Container Registry Location.</span></span>
<span data-ttu-id="31004-119">預設為資源群組的位置。</span><span class="sxs-lookup"><span data-stu-id="31004-119">Default to the location of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31004-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="31004-120">-Name</span></span>
<span data-ttu-id="31004-121">容器登錄名。</span><span class="sxs-lookup"><span data-stu-id="31004-121">Container Registry Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31004-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31004-122">-ResourceGroupName</span></span>
<span data-ttu-id="31004-123">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="31004-123">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31004-124">-Sku</span><span class="sxs-lookup"><span data-stu-id="31004-124">-Sku</span></span>
<span data-ttu-id="31004-125">容器註冊 SKU。</span><span class="sxs-lookup"><span data-stu-id="31004-125">Container Registry SKU.</span></span>
<span data-ttu-id="31004-126">允許的值：基本。</span><span class="sxs-lookup"><span data-stu-id="31004-126">Allowed values: Basic.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ContainerRegistrySku, RegistrySku
Accepted values: Basic

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31004-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="31004-127">-StorageAccountName</span></span>
<span data-ttu-id="31004-128">現有儲存空間帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="31004-128">The name of an existing storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31004-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="31004-129">-Tag</span></span>
<span data-ttu-id="31004-130">以雜湊資料表形式顯示的索引鍵值對。</span><span class="sxs-lookup"><span data-stu-id="31004-130">Container Registry Tags.Key-value pairs in the form of a hash table.</span></span>
<span data-ttu-id="31004-131">例如：</span><span class="sxs-lookup"><span data-stu-id="31004-131">For example:</span></span>

<span data-ttu-id="31004-132">@ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="31004-132">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31004-133">-確認</span><span class="sxs-lookup"><span data-stu-id="31004-133">-Confirm</span></span>
<span data-ttu-id="31004-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="31004-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31004-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31004-135">-WhatIf</span></span>
<span data-ttu-id="31004-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="31004-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="31004-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="31004-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="31004-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31004-138">-DefaultProfile</span></span>
<span data-ttu-id="31004-139">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="31004-139">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="31004-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31004-140">CommonParameters</span></span>
<span data-ttu-id="31004-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="31004-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31004-142">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="31004-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31004-143">輸入</span><span class="sxs-lookup"><span data-stu-id="31004-143">INPUTS</span></span>

### <span data-ttu-id="31004-144">所有</span><span class="sxs-lookup"><span data-stu-id="31004-144">None</span></span>
<span data-ttu-id="31004-145">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="31004-145">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="31004-146">輸出</span><span class="sxs-lookup"><span data-stu-id="31004-146">OUTPUTS</span></span>

### <span data-ttu-id="31004-147">PSContainerRegistry 中的 ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="31004-147">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="31004-148">筆記</span><span class="sxs-lookup"><span data-stu-id="31004-148">NOTES</span></span>

## <span data-ttu-id="31004-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="31004-149">RELATED LINKS</span></span>

[<span data-ttu-id="31004-150">AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="31004-150">Get-AzureRmContainerRegistry</span></span>](Get-AzureRmContainerRegistry.md)

[<span data-ttu-id="31004-151">更新-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="31004-151">Update-AzureRmContainerRegistry</span></span>](Update-AzureRmContainerRegistry.md)

[<span data-ttu-id="31004-152">移除-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="31004-152">Remove-AzureRmContainerRegistry</span></span>](Remove-AzureRmContainerRegistry.md)

