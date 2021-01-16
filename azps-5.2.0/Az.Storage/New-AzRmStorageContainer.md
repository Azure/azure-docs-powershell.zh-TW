---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azrmstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageContainer.md
ms.openlocfilehash: 06a37226c1915ef858d72ec123dd238011c19f19
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98273747"
---
# <span data-ttu-id="81c69-101">New-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="81c69-101">New-AzRmStorageContainer</span></span>

## <span data-ttu-id="81c69-102">摘要</span><span class="sxs-lookup"><span data-stu-id="81c69-102">SYNOPSIS</span></span>
<span data-ttu-id="81c69-103">建立儲存 blob 容器</span><span class="sxs-lookup"><span data-stu-id="81c69-103">Creates a Storage blob container</span></span>

## <span data-ttu-id="81c69-104">句法</span><span class="sxs-lookup"><span data-stu-id="81c69-104">SYNTAX</span></span>

### <span data-ttu-id="81c69-105">AccountName (預設) </span><span class="sxs-lookup"><span data-stu-id="81c69-105">AccountName (Default)</span></span>
```
New-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81c69-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="81c69-106">AccountObject</span></span>
```
New-AzRmStorageContainer -StorageAccount <PSStorageAccount> -Name <String> [-PublicAccess <PSPublicAccess>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81c69-107">說明</span><span class="sxs-lookup"><span data-stu-id="81c69-107">DESCRIPTION</span></span>
<span data-ttu-id="81c69-108">**新的-AzRmStorageContainer** Cmdlet 會建立儲存 blob 容器</span><span class="sxs-lookup"><span data-stu-id="81c69-108">The **New-AzRmStorageContainer** cmdlet creates a Storage blob container</span></span>

## <span data-ttu-id="81c69-109">示例</span><span class="sxs-lookup"><span data-stu-id="81c69-109">EXAMPLES</span></span>

### <span data-ttu-id="81c69-110">範例1：使用儲存空間帳戶名稱和容器名稱（含中繼資料）建立儲存 blob 容器</span><span class="sxs-lookup"><span data-stu-id="81c69-110">Example 1: Create a Storage blob container with Storage account name and container name, with metadata</span></span>
```
PS C:\>New-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Metadata @{tag0="value0";tag1="value1";tag2="value2"}
```

<span data-ttu-id="81c69-111">這個命令會建立含中繼資料之儲存空間帳戶名稱和容器名稱的儲存 blob 容器。</span><span class="sxs-lookup"><span data-stu-id="81c69-111">This command creates a Storage blob container with Storage account name and container name, with metadata.</span></span>

### <span data-ttu-id="81c69-112">範例2：使用儲存空間帳戶物件和容器名稱建立儲存 blob 容器，並以 Blob 公用存取</span><span class="sxs-lookup"><span data-stu-id="81c69-112">Example 2: Create a Storage blob container with Storage account object and container name, with public access as Blob</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>New-AzRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer" -PublicAccess Blob
```

<span data-ttu-id="81c69-113">這個命令會建立含儲存空間帳戶物件和容器名稱的儲存 blob 容器，並以 Blob 公開存取權。</span><span class="sxs-lookup"><span data-stu-id="81c69-113">This command creates a Storage blob container with Storage account object and container name, with public access as Blob.</span></span>

## <span data-ttu-id="81c69-114">參數</span><span class="sxs-lookup"><span data-stu-id="81c69-114">PARAMETERS</span></span>

### <span data-ttu-id="81c69-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81c69-115">-DefaultProfile</span></span>
<span data-ttu-id="81c69-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="81c69-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="81c69-117">-中繼資料</span><span class="sxs-lookup"><span data-stu-id="81c69-117">-Metadata</span></span>
<span data-ttu-id="81c69-118">容器中繼資料</span><span class="sxs-lookup"><span data-stu-id="81c69-118">Container Metadata</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81c69-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="81c69-119">-Name</span></span>
<span data-ttu-id="81c69-120">容器名稱</span><span class="sxs-lookup"><span data-stu-id="81c69-120">Container Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, ContainerName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="81c69-121">-PublicAccess</span><span class="sxs-lookup"><span data-stu-id="81c69-121">-PublicAccess</span></span>
<span data-ttu-id="81c69-122">容器 PublicAccess</span><span class="sxs-lookup"><span data-stu-id="81c69-122">Container PublicAccess</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSPublicAccess
Parameter Sets: (All)
Aliases:
Accepted values: Container, Blob, None

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81c69-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81c69-123">-ResourceGroupName</span></span>
<span data-ttu-id="81c69-124">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="81c69-124">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81c69-125">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="81c69-125">-StorageAccount</span></span>
<span data-ttu-id="81c69-126">儲存空間帳戶物件</span><span class="sxs-lookup"><span data-stu-id="81c69-126">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="81c69-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="81c69-127">-StorageAccountName</span></span>
<span data-ttu-id="81c69-128">儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="81c69-128">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81c69-129">-確認</span><span class="sxs-lookup"><span data-stu-id="81c69-129">-Confirm</span></span>
<span data-ttu-id="81c69-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="81c69-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81c69-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81c69-131">-WhatIf</span></span>
<span data-ttu-id="81c69-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="81c69-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="81c69-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="81c69-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81c69-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81c69-134">CommonParameters</span></span>
<span data-ttu-id="81c69-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="81c69-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81c69-136">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="81c69-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81c69-137">輸入</span><span class="sxs-lookup"><span data-stu-id="81c69-137">INPUTS</span></span>

### <span data-ttu-id="81c69-138">System.object</span><span class="sxs-lookup"><span data-stu-id="81c69-138">System.String</span></span>

### <span data-ttu-id="81c69-139">PSStorageAccount 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="81c69-139">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="81c69-140">輸出</span><span class="sxs-lookup"><span data-stu-id="81c69-140">OUTPUTS</span></span>

### <span data-ttu-id="81c69-141">PSContainer 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="81c69-141">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="81c69-142">筆記</span><span class="sxs-lookup"><span data-stu-id="81c69-142">NOTES</span></span>

## <span data-ttu-id="81c69-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="81c69-143">RELATED LINKS</span></span>
