---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azrmstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageContainer.md
ms.openlocfilehash: f15d9905abbc7a61dc77d4e8b28c5942126d7b14
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93614634"
---
# <span data-ttu-id="dddb2-101">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="dddb2-101">Get-AzRmStorageContainer</span></span>

## <span data-ttu-id="dddb2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="dddb2-102">SYNOPSIS</span></span>
<span data-ttu-id="dddb2-103">取得或列出儲存 blob 容器</span><span class="sxs-lookup"><span data-stu-id="dddb2-103">Gets or lists Storage blob containers</span></span>

## <span data-ttu-id="dddb2-104">句法</span><span class="sxs-lookup"><span data-stu-id="dddb2-104">SYNTAX</span></span>

### <span data-ttu-id="dddb2-105">AccountName (預設) </span><span class="sxs-lookup"><span data-stu-id="dddb2-105">AccountName (Default)</span></span>
```
Get-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dddb2-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="dddb2-106">AccountObject</span></span>
```
Get-AzRmStorageContainer -StorageAccount <PSStorageAccount> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dddb2-107">說明</span><span class="sxs-lookup"><span data-stu-id="dddb2-107">DESCRIPTION</span></span>
<span data-ttu-id="dddb2-108">**AzRmStorageContainer** Cmdlet 會取得或列出儲存 blob 容器</span><span class="sxs-lookup"><span data-stu-id="dddb2-108">The **Get-AzRmStorageContainer** cmdlet gets or lists  Storage blob containers</span></span>

## <span data-ttu-id="dddb2-109">示例</span><span class="sxs-lookup"><span data-stu-id="dddb2-109">EXAMPLES</span></span>

### <span data-ttu-id="dddb2-110">範例1：使用儲存空間帳戶名稱和容器名稱來取得儲存 blob 容器</span><span class="sxs-lookup"><span data-stu-id="dddb2-110">Example 1: Get a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Get-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
```

<span data-ttu-id="dddb2-111">這個命令會取得含儲存空間帳戶名稱和容器名稱的儲存 blob 容器。</span><span class="sxs-lookup"><span data-stu-id="dddb2-111">This command gets a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="dddb2-112">範例2：列出儲存空間帳戶的所有儲存 blob 容器</span><span class="sxs-lookup"><span data-stu-id="dddb2-112">Example 2: List  all Storage blob containers of a Storage account</span></span>
```
PS C:\>Get-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
```

<span data-ttu-id="dddb2-113">這個命令會列出含儲存空間帳戶名稱的儲存空間帳戶的所有儲存 blob 容器。</span><span class="sxs-lookup"><span data-stu-id="dddb2-113">This command lists all Storage blob containers of a Storage account with Storage account name.</span></span>

### <span data-ttu-id="dddb2-114">範例3：使用儲存空間帳戶物件和容器名稱來取得儲存 blob 容器。</span><span class="sxs-lookup"><span data-stu-id="dddb2-114">Example 3: Get a Storage blob container with Storage account object and container name.</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Get-AzRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer"
```

<span data-ttu-id="dddb2-115">這個命令會取得含儲存空間帳戶物件和容器名稱的儲存 blob 容器。</span><span class="sxs-lookup"><span data-stu-id="dddb2-115">This command gets a Storage blob container with Storage account object and container name.</span></span>

## <span data-ttu-id="dddb2-116">參數</span><span class="sxs-lookup"><span data-stu-id="dddb2-116">PARAMETERS</span></span>

### <span data-ttu-id="dddb2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dddb2-117">-DefaultProfile</span></span>
<span data-ttu-id="dddb2-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="dddb2-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dddb2-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="dddb2-119">-Name</span></span>
<span data-ttu-id="dddb2-120">容器名稱</span><span class="sxs-lookup"><span data-stu-id="dddb2-120">Container Name</span></span>

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

### <span data-ttu-id="dddb2-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dddb2-121">-ResourceGroupName</span></span>
<span data-ttu-id="dddb2-122">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="dddb2-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="dddb2-123">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="dddb2-123">-StorageAccount</span></span>
<span data-ttu-id="dddb2-124">儲存空間帳戶物件</span><span class="sxs-lookup"><span data-stu-id="dddb2-124">Storage account object</span></span>

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

### <span data-ttu-id="dddb2-125">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="dddb2-125">-StorageAccountName</span></span>
<span data-ttu-id="dddb2-126">儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="dddb2-126">Storage Account Name.</span></span>

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

### <span data-ttu-id="dddb2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dddb2-127">CommonParameters</span></span>
<span data-ttu-id="dddb2-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="dddb2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dddb2-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="dddb2-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dddb2-130">輸入</span><span class="sxs-lookup"><span data-stu-id="dddb2-130">INPUTS</span></span>

### <span data-ttu-id="dddb2-131">System.object</span><span class="sxs-lookup"><span data-stu-id="dddb2-131">System.String</span></span>

### <span data-ttu-id="dddb2-132">PSStorageAccount 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="dddb2-132">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="dddb2-133">輸出</span><span class="sxs-lookup"><span data-stu-id="dddb2-133">OUTPUTS</span></span>

### <span data-ttu-id="dddb2-134">PSContainer 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="dddb2-134">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="dddb2-135">筆記</span><span class="sxs-lookup"><span data-stu-id="dddb2-135">NOTES</span></span>

## <span data-ttu-id="dddb2-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="dddb2-136">RELATED LINKS</span></span>
