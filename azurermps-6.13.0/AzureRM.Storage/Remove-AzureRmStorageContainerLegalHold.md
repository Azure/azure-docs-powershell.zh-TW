---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/remove-azurermstoragecontainerlegalhold
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Remove-AzureRmStorageContainerLegalHold.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Remove-AzureRmStorageContainerLegalHold.md
ms.openlocfilehash: da0793e7eb10f7b83d785aea34866842abe9b887
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450158"
---
# <span data-ttu-id="30c6b-101">Remove-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="30c6b-101">Remove-AzureRmStorageContainerLegalHold</span></span>

## <span data-ttu-id="30c6b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="30c6b-102">SYNOPSIS</span></span>
<span data-ttu-id="30c6b-103">從儲存 blob 容器中移除合法保留標籤</span><span class="sxs-lookup"><span data-stu-id="30c6b-103">Removes legal hold tags from a Storage blob container</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="30c6b-104">句法</span><span class="sxs-lookup"><span data-stu-id="30c6b-104">SYNTAX</span></span>

### <span data-ttu-id="30c6b-105">AccountName (預設) </span><span class="sxs-lookup"><span data-stu-id="30c6b-105">AccountName (Default)</span></span>
```
Remove-AzureRmStorageContainerLegalHold [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -Name <String> -Tag <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="30c6b-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="30c6b-106">AccountObject</span></span>
```
Remove-AzureRmStorageContainerLegalHold -Name <String> -StorageAccount <PSStorageAccount> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30c6b-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="30c6b-107">ContainerObject</span></span>
```
Remove-AzureRmStorageContainerLegalHold -Container <PSContainer> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30c6b-108">說明</span><span class="sxs-lookup"><span data-stu-id="30c6b-108">DESCRIPTION</span></span>
<span data-ttu-id="30c6b-109">**AzureRmStorageContainerLegalHold** Cmdlet 會從儲存 blob 容器中移除合法保留標籤</span><span class="sxs-lookup"><span data-stu-id="30c6b-109">The **Remove-AzureRmStorageContainerLegalHold** cmdlet removes legal hold tags from a Storage blob container</span></span>

## <span data-ttu-id="30c6b-110">示例</span><span class="sxs-lookup"><span data-stu-id="30c6b-110">EXAMPLES</span></span>

### <span data-ttu-id="30c6b-111">範例1：從含儲存空間帳戶名稱和容器名稱的儲存 blob 容器中移除合法保留標記</span><span class="sxs-lookup"><span data-stu-id="30c6b-111">Example 1: Remove legal hold tags from a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Remove-AzureRmStorageContainerLegalHold -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Tag  tag1
```

<span data-ttu-id="30c6b-112">這個命令會從儲存區名稱和容器名稱中移除儲存 blob 容器中的合法保留標籤。</span><span class="sxs-lookup"><span data-stu-id="30c6b-112">This command removes legal hold tags from a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="30c6b-113">範例2：從含儲存空間帳戶物件和容器名稱的儲存 blob 容器中移除合法保留標記</span><span class="sxs-lookup"><span data-stu-id="30c6b-113">Example 2: Remove legal hold tags from a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzureRmStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Remove-AzureRmStorageContainerLegalHold -StorageAccount $accountObject -ContainerName "myContainer"  -Tag  tag1,tag2 
```

<span data-ttu-id="30c6b-114">這個命令會從含儲存空間帳戶物件和容器名稱的儲存 blob 容器中移除合法保留標籤。</span><span class="sxs-lookup"><span data-stu-id="30c6b-114">This command removes legal hold tags from a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="30c6b-115">範例3：從含管線的儲存空間帳戶中的所有儲存區 blob 容器移除合法保留標籤</span><span class="sxs-lookup"><span data-stu-id="30c6b-115">Example 3: Remove legal hold tags from all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Remove-AzureRmStorageContainerLegalHold -Tag  tag1
```

<span data-ttu-id="30c6b-116">這個命令會從含管線的儲存空間帳戶中的所有儲存區 blob 容器中移除合法保留標籤。</span><span class="sxs-lookup"><span data-stu-id="30c6b-116">This command removes legal hold tags from all Storage blob containers in a Storage account with pipeline.</span></span>


## <span data-ttu-id="30c6b-117">參數</span><span class="sxs-lookup"><span data-stu-id="30c6b-117">PARAMETERS</span></span>

### <span data-ttu-id="30c6b-118">-容器</span><span class="sxs-lookup"><span data-stu-id="30c6b-118">-Container</span></span>
<span data-ttu-id="30c6b-119">儲存容器物件</span><span class="sxs-lookup"><span data-stu-id="30c6b-119">Storage container object</span></span>

```yaml
Type: PSContainer
Parameter Sets: ContainerObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="30c6b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30c6b-120">-DefaultProfile</span></span>
<span data-ttu-id="30c6b-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="30c6b-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="30c6b-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="30c6b-122">-Name</span></span>
<span data-ttu-id="30c6b-123">容器名稱</span><span class="sxs-lookup"><span data-stu-id="30c6b-123">Container Name</span></span>

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

### <span data-ttu-id="30c6b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30c6b-124">-ResourceGroupName</span></span>
<span data-ttu-id="30c6b-125">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="30c6b-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="30c6b-126">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="30c6b-126">-StorageAccount</span></span>
<span data-ttu-id="30c6b-127">儲存空間帳戶物件</span><span class="sxs-lookup"><span data-stu-id="30c6b-127">Storage account object</span></span>

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

### <span data-ttu-id="30c6b-128">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="30c6b-128">-StorageAccountName</span></span>
<span data-ttu-id="30c6b-129">儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="30c6b-129">Storage Account Name.</span></span>

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

### <span data-ttu-id="30c6b-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="30c6b-130">-Tag</span></span>
<span data-ttu-id="30c6b-131">容器 LegalHold 標記</span><span class="sxs-lookup"><span data-stu-id="30c6b-131">Container LegalHold Tags</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30c6b-132">-確認</span><span class="sxs-lookup"><span data-stu-id="30c6b-132">-Confirm</span></span>
<span data-ttu-id="30c6b-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="30c6b-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30c6b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30c6b-134">-WhatIf</span></span>
<span data-ttu-id="30c6b-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="30c6b-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="30c6b-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="30c6b-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30c6b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30c6b-137">CommonParameters</span></span>
<span data-ttu-id="30c6b-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="30c6b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30c6b-139">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="30c6b-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30c6b-140">輸入</span><span class="sxs-lookup"><span data-stu-id="30c6b-140">INPUTS</span></span>

### <span data-ttu-id="30c6b-141">System.object</span><span class="sxs-lookup"><span data-stu-id="30c6b-141">System.String</span></span>

## <span data-ttu-id="30c6b-142">輸出</span><span class="sxs-lookup"><span data-stu-id="30c6b-142">OUTPUTS</span></span>

### <span data-ttu-id="30c6b-143">PSLegalHold 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="30c6b-143">Microsoft.Azure.Commands.Management.Storage.Models.PSLegalHold</span></span>

## <span data-ttu-id="30c6b-144">筆記</span><span class="sxs-lookup"><span data-stu-id="30c6b-144">NOTES</span></span>

## <span data-ttu-id="30c6b-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="30c6b-145">RELATED LINKS</span></span>

