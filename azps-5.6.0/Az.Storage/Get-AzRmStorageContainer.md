---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azrmstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageContainer.md
ms.openlocfilehash: c4f5fe5fa703d2706d37cd0bebf9df79fd272f5b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915181"
---
# <span data-ttu-id="1c62c-101">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="1c62c-101">Get-AzRmStorageContainer</span></span>

## <span data-ttu-id="1c62c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="1c62c-102">SYNOPSIS</span></span>
<span data-ttu-id="1c62c-103">獲取或列出儲存 Blob 容器</span><span class="sxs-lookup"><span data-stu-id="1c62c-103">Gets or lists Storage blob containers</span></span>

## <span data-ttu-id="1c62c-104">語法</span><span class="sxs-lookup"><span data-stu-id="1c62c-104">SYNTAX</span></span>

### <span data-ttu-id="1c62c-105">AccountName (預設) </span><span class="sxs-lookup"><span data-stu-id="1c62c-105">AccountName (Default)</span></span>
```
Get-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1c62c-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="1c62c-106">AccountObject</span></span>
```
Get-AzRmStorageContainer -StorageAccount <PSStorageAccount> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1c62c-107">描述</span><span class="sxs-lookup"><span data-stu-id="1c62c-107">DESCRIPTION</span></span>
<span data-ttu-id="1c62c-108">**Get-AzRmStorageContainer Cmdlet** 取得或列出儲存 Blob 容器</span><span class="sxs-lookup"><span data-stu-id="1c62c-108">The **Get-AzRmStorageContainer** cmdlet gets or lists  Storage blob containers</span></span>

## <span data-ttu-id="1c62c-109">例子</span><span class="sxs-lookup"><span data-stu-id="1c62c-109">EXAMPLES</span></span>

### <span data-ttu-id="1c62c-110">範例 1：取得儲存空間 Blob 容器與儲存帳戶名稱和容器名稱</span><span class="sxs-lookup"><span data-stu-id="1c62c-110">Example 1: Get a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Get-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
```

<span data-ttu-id="1c62c-111">此命令會獲得包含儲存帳戶名稱和容器名稱的儲存 Blob 容器。</span><span class="sxs-lookup"><span data-stu-id="1c62c-111">This command gets a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="1c62c-112">範例 2：列出儲存帳戶的所有儲存 Blob 容器</span><span class="sxs-lookup"><span data-stu-id="1c62c-112">Example 2: List  all Storage blob containers of a Storage account</span></span>
```
PS C:\>Get-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
```

<span data-ttu-id="1c62c-113">此命令會以儲存帳戶名稱列出儲存帳戶的所有儲存 Blob 容器。</span><span class="sxs-lookup"><span data-stu-id="1c62c-113">This command lists all Storage blob containers of a Storage account with Storage account name.</span></span>

### <span data-ttu-id="1c62c-114">範例 3：取得儲存空間 Blob 容器與儲存帳戶物件和容器名稱。</span><span class="sxs-lookup"><span data-stu-id="1c62c-114">Example 3: Get a Storage blob container with Storage account object and container name.</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Get-AzRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer"
```

<span data-ttu-id="1c62c-115">此命令會獲得包含儲存帳戶物件和容器名稱的儲存 Blob 容器。</span><span class="sxs-lookup"><span data-stu-id="1c62c-115">This command gets a Storage blob container with Storage account object and container name.</span></span>

## <span data-ttu-id="1c62c-116">參數</span><span class="sxs-lookup"><span data-stu-id="1c62c-116">PARAMETERS</span></span>

### <span data-ttu-id="1c62c-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1c62c-117">-AsJob</span></span>
<span data-ttu-id="1c62c-118">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="1c62c-118">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c62c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c62c-119">-DefaultProfile</span></span>
<span data-ttu-id="1c62c-120">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="1c62c-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1c62c-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="1c62c-121">-Name</span></span>
<span data-ttu-id="1c62c-122">容器名稱</span><span class="sxs-lookup"><span data-stu-id="1c62c-122">Container Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, ContainerName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1c62c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c62c-123">-ResourceGroupName</span></span>
<span data-ttu-id="1c62c-124">資源組名。</span><span class="sxs-lookup"><span data-stu-id="1c62c-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="1c62c-125">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="1c62c-125">-StorageAccount</span></span>
<span data-ttu-id="1c62c-126">儲存空間帳戶物件</span><span class="sxs-lookup"><span data-stu-id="1c62c-126">Storage account object</span></span>

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

### <span data-ttu-id="1c62c-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="1c62c-127">-StorageAccountName</span></span>
<span data-ttu-id="1c62c-128">儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="1c62c-128">Storage Account Name.</span></span>

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

### <span data-ttu-id="1c62c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c62c-129">CommonParameters</span></span>
<span data-ttu-id="1c62c-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="1c62c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c62c-131">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="1c62c-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c62c-132">輸入</span><span class="sxs-lookup"><span data-stu-id="1c62c-132">INPUTS</span></span>

### <span data-ttu-id="1c62c-133">System.String</span><span class="sxs-lookup"><span data-stu-id="1c62c-133">System.String</span></span>

### <span data-ttu-id="1c62c-134">Microsoft.Azure.Commands.management.storage.models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1c62c-134">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="1c62c-135">輸出</span><span class="sxs-lookup"><span data-stu-id="1c62c-135">OUTPUTS</span></span>

### <span data-ttu-id="1c62c-136">Microsoft.Azure.Commands.management.storage.models.PSContainer</span><span class="sxs-lookup"><span data-stu-id="1c62c-136">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="1c62c-137">筆記</span><span class="sxs-lookup"><span data-stu-id="1c62c-137">NOTES</span></span>

## <span data-ttu-id="1c62c-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="1c62c-138">RELATED LINKS</span></span>
