---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/get-azurermstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageContainer.md
ms.openlocfilehash: 64e3857ddd9a9bb00b94e3e550c6be33722990a3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445379"
---
# <span data-ttu-id="18082-101">Get-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="18082-101">Get-AzureRmStorageContainer</span></span>

## <span data-ttu-id="18082-102">摘要</span><span class="sxs-lookup"><span data-stu-id="18082-102">SYNOPSIS</span></span>
<span data-ttu-id="18082-103">取得或列出儲存 blob 容器</span><span class="sxs-lookup"><span data-stu-id="18082-103">Gets or lists Storage blob containers</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="18082-104">句法</span><span class="sxs-lookup"><span data-stu-id="18082-104">SYNTAX</span></span>

### <span data-ttu-id="18082-105">AccountName (預設) </span><span class="sxs-lookup"><span data-stu-id="18082-105">AccountName (Default)</span></span>
```
Get-AzureRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="18082-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="18082-106">AccountObject</span></span>
```
Get-AzureRmStorageContainer -StorageAccount <PSStorageAccount> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="18082-107">說明</span><span class="sxs-lookup"><span data-stu-id="18082-107">DESCRIPTION</span></span>
<span data-ttu-id="18082-108">**AzureRmStorageContainer** Cmdlet 會取得或列出儲存 blob 容器</span><span class="sxs-lookup"><span data-stu-id="18082-108">The **Get-AzureRmStorageContainer** cmdlet gets or lists  Storage blob containers</span></span>

## <span data-ttu-id="18082-109">示例</span><span class="sxs-lookup"><span data-stu-id="18082-109">EXAMPLES</span></span>

### <span data-ttu-id="18082-110">範例1：使用儲存空間帳戶名稱和容器名稱來取得儲存 blob 容器</span><span class="sxs-lookup"><span data-stu-id="18082-110">Example 1: Get a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Get-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" 
```

<span data-ttu-id="18082-111">這個命令會取得含儲存空間帳戶名稱和容器名稱的儲存 blob 容器。</span><span class="sxs-lookup"><span data-stu-id="18082-111">This command gets a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="18082-112">範例2：列出儲存空間帳戶的所有儲存 blob 容器</span><span class="sxs-lookup"><span data-stu-id="18082-112">Example 2: List  all Storage blob containers of a Storage account</span></span>
```
PS C:\>Get-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" 
```

<span data-ttu-id="18082-113">這個命令會列出含儲存空間帳戶名稱的儲存空間帳戶的所有儲存 blob 容器。</span><span class="sxs-lookup"><span data-stu-id="18082-113">This command lists all Storage blob containers of a Storage account with Storage account name.</span></span>

### <span data-ttu-id="18082-114">範例3：使用儲存空間帳戶物件和容器名稱來取得儲存 blob 容器。</span><span class="sxs-lookup"><span data-stu-id="18082-114">Example 3: Get a Storage blob container with Storage account object and container name.</span></span>
```
PS C:\>$accountObject = Get-AzureRmStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Get-AzureRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer" 
```

<span data-ttu-id="18082-115">這個命令會取得含儲存空間帳戶物件和容器名稱的儲存 blob 容器。</span><span class="sxs-lookup"><span data-stu-id="18082-115">This command gets a Storage blob container with Storage account object and container name.</span></span>

## <span data-ttu-id="18082-116">參數</span><span class="sxs-lookup"><span data-stu-id="18082-116">PARAMETERS</span></span>

### <span data-ttu-id="18082-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18082-117">-DefaultProfile</span></span>
<span data-ttu-id="18082-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="18082-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="18082-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="18082-119">-Name</span></span>
<span data-ttu-id="18082-120">容器名稱</span><span class="sxs-lookup"><span data-stu-id="18082-120">Container Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, ContainerName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="18082-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18082-121">-ResourceGroupName</span></span>
<span data-ttu-id="18082-122">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="18082-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="18082-123">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="18082-123">-StorageAccount</span></span>
<span data-ttu-id="18082-124">儲存空間帳戶物件</span><span class="sxs-lookup"><span data-stu-id="18082-124">Storage account object</span></span>

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

### <span data-ttu-id="18082-125">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="18082-125">-StorageAccountName</span></span>
<span data-ttu-id="18082-126">儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="18082-126">Storage Account Name.</span></span>

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

### <span data-ttu-id="18082-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18082-127">CommonParameters</span></span>
<span data-ttu-id="18082-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="18082-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18082-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="18082-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18082-130">輸入</span><span class="sxs-lookup"><span data-stu-id="18082-130">INPUTS</span></span>

### <span data-ttu-id="18082-131">System.object</span><span class="sxs-lookup"><span data-stu-id="18082-131">System.String</span></span>

## <span data-ttu-id="18082-132">輸出</span><span class="sxs-lookup"><span data-stu-id="18082-132">OUTPUTS</span></span>

### <span data-ttu-id="18082-133">PSContainer 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="18082-133">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="18082-134">筆記</span><span class="sxs-lookup"><span data-stu-id="18082-134">NOTES</span></span>

## <span data-ttu-id="18082-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="18082-135">RELATED LINKS</span></span>

