---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/remove-azurermstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Remove-AzureRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Remove-AzureRmStorageContainer.md
ms.openlocfilehash: 089451a0a0aae399a18296fbf4982724b35d432e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626033"
---
# <span data-ttu-id="449e9-101">Remove-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="449e9-101">Remove-AzureRmStorageContainer</span></span>

## <span data-ttu-id="449e9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="449e9-102">SYNOPSIS</span></span>
<span data-ttu-id="449e9-103">移除儲存 blob 容器</span><span class="sxs-lookup"><span data-stu-id="449e9-103">Removes a Storage blob container</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="449e9-104">句法</span><span class="sxs-lookup"><span data-stu-id="449e9-104">SYNTAX</span></span>

### <span data-ttu-id="449e9-105">AccountName (預設) </span><span class="sxs-lookup"><span data-stu-id="449e9-105">AccountName (Default)</span></span>
```
Remove-AzureRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="449e9-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="449e9-106">AccountObject</span></span>
```
Remove-AzureRmStorageContainer -Name <String> -StorageAccount <PSStorageAccount> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="449e9-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="449e9-107">ContainerObject</span></span>
```
Remove-AzureRmStorageContainer -InputObject <PSContainer> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="449e9-108">說明</span><span class="sxs-lookup"><span data-stu-id="449e9-108">DESCRIPTION</span></span>
<span data-ttu-id="449e9-109">**AzureRmStorageContainer** Cmdlet 會移除存儲 blob 容器</span><span class="sxs-lookup"><span data-stu-id="449e9-109">The **Remove-AzureRmStorageContainer** cmdlet removes a Storage blob container</span></span>

## <span data-ttu-id="449e9-110">示例</span><span class="sxs-lookup"><span data-stu-id="449e9-110">EXAMPLES</span></span>

### <span data-ttu-id="449e9-111">範例1：移除含儲存空間帳戶名稱和容器名稱的儲存 blob 容器</span><span class="sxs-lookup"><span data-stu-id="449e9-111">Example 1: Remove a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Remove-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
```

<span data-ttu-id="449e9-112">這個命令會移除儲存空間帳戶名稱和容器名稱的儲存 blob 容器。</span><span class="sxs-lookup"><span data-stu-id="449e9-112">This command removes a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="449e9-113">範例2：移除含儲存空間帳戶物件和容器名稱的儲存 blob 容器</span><span class="sxs-lookup"><span data-stu-id="449e9-113">Example 2: Remove a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzureRmStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Remove-AzureRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer"
```

<span data-ttu-id="449e9-114">這個命令會移除含儲存空間帳戶物件和容器名稱的儲存 blob 容器。</span><span class="sxs-lookup"><span data-stu-id="449e9-114">This command removes a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="449e9-115">範例3：移除包含管線的儲存空間帳戶中的所有儲存 blob 容器</span><span class="sxs-lookup"><span data-stu-id="449e9-115">Example 3: Remove all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Remove-AzureRmStorageContainer -Force
```

<span data-ttu-id="449e9-116">這個命令會移除含管線的儲存空間帳戶中的所有儲存 blob 容器。</span><span class="sxs-lookup"><span data-stu-id="449e9-116">This command removes all Storage blob containers in a Storage account with pipeline.</span></span>

## <span data-ttu-id="449e9-117">參數</span><span class="sxs-lookup"><span data-stu-id="449e9-117">PARAMETERS</span></span>

### <span data-ttu-id="449e9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="449e9-118">-DefaultProfile</span></span>
<span data-ttu-id="449e9-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="449e9-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="449e9-120">-Force</span><span class="sxs-lookup"><span data-stu-id="449e9-120">-Force</span></span>
<span data-ttu-id="449e9-121">強制移除容器及其中的所有內容</span><span class="sxs-lookup"><span data-stu-id="449e9-121">Force to remove the container and all content in it</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="449e9-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="449e9-122">-InputObject</span></span>
<span data-ttu-id="449e9-123">儲存容器物件</span><span class="sxs-lookup"><span data-stu-id="449e9-123">Storage container object</span></span>

```yaml
Type: PSContainer
Parameter Sets: ContainerObject
Aliases: Container

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="449e9-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="449e9-124">-Name</span></span>
<span data-ttu-id="449e9-125">容器名稱</span><span class="sxs-lookup"><span data-stu-id="449e9-125">Container Name</span></span>

```yaml
Type: String
Parameter Sets: AccountName, AccountObject
Aliases: N, ContainerName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="449e9-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="449e9-126">-PassThru</span></span>
<span data-ttu-id="449e9-127">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="449e9-127">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="449e9-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="449e9-128">-ResourceGroupName</span></span>
<span data-ttu-id="449e9-129">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="449e9-129">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="449e9-130">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="449e9-130">-StorageAccount</span></span>
<span data-ttu-id="449e9-131">儲存空間帳戶物件</span><span class="sxs-lookup"><span data-stu-id="449e9-131">Storage account object</span></span>

```yaml
Type: PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="449e9-132">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="449e9-132">-StorageAccountName</span></span>
<span data-ttu-id="449e9-133">儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="449e9-133">Storage Account Name.</span></span>

```yaml
Type: String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="449e9-134">-確認</span><span class="sxs-lookup"><span data-stu-id="449e9-134">-Confirm</span></span>
<span data-ttu-id="449e9-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="449e9-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="449e9-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="449e9-136">-WhatIf</span></span>
<span data-ttu-id="449e9-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="449e9-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="449e9-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="449e9-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="449e9-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="449e9-139">CommonParameters</span></span>
<span data-ttu-id="449e9-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="449e9-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="449e9-141">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="449e9-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="449e9-142">輸入</span><span class="sxs-lookup"><span data-stu-id="449e9-142">INPUTS</span></span>

### <span data-ttu-id="449e9-143">System.object</span><span class="sxs-lookup"><span data-stu-id="449e9-143">System.String</span></span>

## <span data-ttu-id="449e9-144">輸出</span><span class="sxs-lookup"><span data-stu-id="449e9-144">OUTPUTS</span></span>

### <span data-ttu-id="449e9-145">System.object</span><span class="sxs-lookup"><span data-stu-id="449e9-145">System.Object</span></span>

## <span data-ttu-id="449e9-146">筆記</span><span class="sxs-lookup"><span data-stu-id="449e9-146">NOTES</span></span>

## <span data-ttu-id="449e9-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="449e9-147">RELATED LINKS</span></span>
