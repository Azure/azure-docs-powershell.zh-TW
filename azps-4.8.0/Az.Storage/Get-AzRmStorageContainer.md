---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azrmstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageContainer.md
ms.openlocfilehash: da0ccdc791318f0a315bea8d2464d8d0852aec8b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93971632"
---
# <span data-ttu-id="cd580-101">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="cd580-101">Get-AzRmStorageContainer</span></span>

## <span data-ttu-id="cd580-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cd580-102">SYNOPSIS</span></span>
<span data-ttu-id="cd580-103">取得或列出儲存 blob 容器</span><span class="sxs-lookup"><span data-stu-id="cd580-103">Gets or lists Storage blob containers</span></span>

## <span data-ttu-id="cd580-104">句法</span><span class="sxs-lookup"><span data-stu-id="cd580-104">SYNTAX</span></span>

### <span data-ttu-id="cd580-105">AccountName (預設) </span><span class="sxs-lookup"><span data-stu-id="cd580-105">AccountName (Default)</span></span>
```
Get-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd580-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="cd580-106">AccountObject</span></span>
```
Get-AzRmStorageContainer -StorageAccount <PSStorageAccount> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cd580-107">說明</span><span class="sxs-lookup"><span data-stu-id="cd580-107">DESCRIPTION</span></span>
<span data-ttu-id="cd580-108">**AzRmStorageContainer** Cmdlet 會取得或列出儲存 blob 容器</span><span class="sxs-lookup"><span data-stu-id="cd580-108">The **Get-AzRmStorageContainer** cmdlet gets or lists  Storage blob containers</span></span>

## <span data-ttu-id="cd580-109">示例</span><span class="sxs-lookup"><span data-stu-id="cd580-109">EXAMPLES</span></span>

### <span data-ttu-id="cd580-110">範例1：使用儲存空間帳戶名稱和容器名稱來取得儲存 blob 容器</span><span class="sxs-lookup"><span data-stu-id="cd580-110">Example 1: Get a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Get-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
```

<span data-ttu-id="cd580-111">這個命令會取得含儲存空間帳戶名稱和容器名稱的儲存 blob 容器。</span><span class="sxs-lookup"><span data-stu-id="cd580-111">This command gets a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="cd580-112">範例2：列出儲存空間帳戶的所有儲存 blob 容器</span><span class="sxs-lookup"><span data-stu-id="cd580-112">Example 2: List  all Storage blob containers of a Storage account</span></span>
```
PS C:\>Get-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
```

<span data-ttu-id="cd580-113">這個命令會列出含儲存空間帳戶名稱的儲存空間帳戶的所有儲存 blob 容器。</span><span class="sxs-lookup"><span data-stu-id="cd580-113">This command lists all Storage blob containers of a Storage account with Storage account name.</span></span>

### <span data-ttu-id="cd580-114">範例3：使用儲存空間帳戶物件和容器名稱來取得儲存 blob 容器。</span><span class="sxs-lookup"><span data-stu-id="cd580-114">Example 3: Get a Storage blob container with Storage account object and container name.</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Get-AzRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer"
```

<span data-ttu-id="cd580-115">這個命令會取得含儲存空間帳戶物件和容器名稱的儲存 blob 容器。</span><span class="sxs-lookup"><span data-stu-id="cd580-115">This command gets a Storage blob container with Storage account object and container name.</span></span>

## <span data-ttu-id="cd580-116">參數</span><span class="sxs-lookup"><span data-stu-id="cd580-116">PARAMETERS</span></span>

### <span data-ttu-id="cd580-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cd580-117">-AsJob</span></span>
<span data-ttu-id="cd580-118">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd580-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cd580-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd580-119">-DefaultProfile</span></span>
<span data-ttu-id="cd580-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cd580-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cd580-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="cd580-121">-Name</span></span>
<span data-ttu-id="cd580-122">容器名稱</span><span class="sxs-lookup"><span data-stu-id="cd580-122">Container Name</span></span>

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

### <span data-ttu-id="cd580-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd580-123">-ResourceGroupName</span></span>
<span data-ttu-id="cd580-124">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="cd580-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="cd580-125">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="cd580-125">-StorageAccount</span></span>
<span data-ttu-id="cd580-126">儲存空間帳戶物件</span><span class="sxs-lookup"><span data-stu-id="cd580-126">Storage account object</span></span>

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

### <span data-ttu-id="cd580-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="cd580-127">-StorageAccountName</span></span>
<span data-ttu-id="cd580-128">儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="cd580-128">Storage Account Name.</span></span>

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

### <span data-ttu-id="cd580-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd580-129">CommonParameters</span></span>
<span data-ttu-id="cd580-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cd580-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd580-131">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="cd580-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd580-132">輸入</span><span class="sxs-lookup"><span data-stu-id="cd580-132">INPUTS</span></span>

### <span data-ttu-id="cd580-133">System.object</span><span class="sxs-lookup"><span data-stu-id="cd580-133">System.String</span></span>

### <span data-ttu-id="cd580-134">PSStorageAccount 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="cd580-134">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="cd580-135">輸出</span><span class="sxs-lookup"><span data-stu-id="cd580-135">OUTPUTS</span></span>

### <span data-ttu-id="cd580-136">PSContainer 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="cd580-136">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="cd580-137">筆記</span><span class="sxs-lookup"><span data-stu-id="cd580-137">NOTES</span></span>

## <span data-ttu-id="cd580-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="cd580-138">RELATED LINKS</span></span>
