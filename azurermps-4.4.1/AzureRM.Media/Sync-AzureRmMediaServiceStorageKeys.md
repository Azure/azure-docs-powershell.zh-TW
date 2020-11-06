---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: F395E192-80FA-421D-A389-8C5C0C2267E4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Sync-AzureRmMediaServiceStorageKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Sync-AzureRmMediaServiceStorageKeys.md
ms.openlocfilehash: 71112bf54f4de8e0c7e4fd1ecfd296eff45ac868
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454340"
---
# <span data-ttu-id="18527-101">Sync-AzureRmMediaServiceStorageKeys</span><span class="sxs-lookup"><span data-stu-id="18527-101">Sync-AzureRmMediaServiceStorageKeys</span></span>

## <span data-ttu-id="18527-102">摘要</span><span class="sxs-lookup"><span data-stu-id="18527-102">SYNOPSIS</span></span>
<span data-ttu-id="18527-103">針對與媒體服務相關聯的儲存空間帳戶同步處理儲存空間帳戶金鑰。</span><span class="sxs-lookup"><span data-stu-id="18527-103">Synchronizes storage account keys for a storage account associated with the media service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="18527-104">句法</span><span class="sxs-lookup"><span data-stu-id="18527-104">SYNTAX</span></span>

```
Sync-AzureRmMediaServiceStorageKeys [-ResourceGroupName] <String> [-AccountName] <String>
 [-StorageAccountId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="18527-105">說明</span><span class="sxs-lookup"><span data-stu-id="18527-105">DESCRIPTION</span></span>
<span data-ttu-id="18527-106">**Sync-AzureRmMediaServiceStorageKeys** Cmdlet 會針對與媒體服務相關聯的儲存空間帳戶同步處理儲存空間帳戶金鑰。</span><span class="sxs-lookup"><span data-stu-id="18527-106">The **Sync-AzureRmMediaServiceStorageKeys** cmdlet synchronizes storage account keys for a storage account associated with the media service.</span></span>

## <span data-ttu-id="18527-107">示例</span><span class="sxs-lookup"><span data-stu-id="18527-107">EXAMPLES</span></span>

### <span data-ttu-id="18527-108">範例1：針對與媒體服務相關聯的儲存空間帳戶同步處理儲存空間帳戶金鑰</span><span class="sxs-lookup"><span data-stu-id="18527-108">Example 1: Synchronize storage account keys for a storage account associated with the media service</span></span>
```
PS C:\>$StorageAccount = Get-AzureRmStorageAccount -ResourceGroupName "ResourceGroup001" -Name "Storage135"
PS C:\> Sync-AzureRmMediaServiceStorageKeys -ResourceGroupName "ResourceGroup001" -AccoutName "MediasService001" -StorageAccoutId $StorageAccount.Id
```

<span data-ttu-id="18527-109">第一個命令使用 Get-AzureRmStorageAccount Cmdlet 來取得名為 Storage135 的 ResourceGroup001 儲存帳戶，並將結果儲存在名為 $StorageAccount 的變數中。</span><span class="sxs-lookup"><span data-stu-id="18527-109">The first command uses the Get-AzureRmStorageAccount cmdlet to get the storage account named Storage135 that belongs to ResourceGroup001 and stores the result in the variable named $StorageAccount.</span></span>

<span data-ttu-id="18527-110">第二個命令會使用 $StorageAccount 變數中包含的 **Id** 屬性，同步處理名為 MediaService001 的媒體服務的儲存空間帳戶金鑰。</span><span class="sxs-lookup"><span data-stu-id="18527-110">The second command synchronizes the storage account keys for the media service named MediaService001 using the **Id** property contained in the $StorageAccount variable.</span></span>

## <span data-ttu-id="18527-111">參數</span><span class="sxs-lookup"><span data-stu-id="18527-111">PARAMETERS</span></span>

### <span data-ttu-id="18527-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="18527-112">-AccountName</span></span>
<span data-ttu-id="18527-113">指定此 Cmdlet 同步處理的媒體服務名稱。</span><span class="sxs-lookup"><span data-stu-id="18527-113">Specifies the name of the media service that this cmdlet synchronizes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18527-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18527-114">-ResourceGroupName</span></span>
<span data-ttu-id="18527-115">指定包含媒體服務之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="18527-115">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="18527-116">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="18527-116">-StorageAccountId</span></span>
<span data-ttu-id="18527-117">指定與媒體服務帳戶相關聯的儲存空間帳戶 ID。</span><span class="sxs-lookup"><span data-stu-id="18527-117">Specifies the storage account ID associated with the media service account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Id

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18527-118">-確認</span><span class="sxs-lookup"><span data-stu-id="18527-118">-Confirm</span></span>
<span data-ttu-id="18527-119">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="18527-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18527-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18527-120">-WhatIf</span></span>
<span data-ttu-id="18527-121">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="18527-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="18527-122">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="18527-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18527-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18527-123">-DefaultProfile</span></span>
<span data-ttu-id="18527-124">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="18527-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="18527-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18527-125">CommonParameters</span></span>
<span data-ttu-id="18527-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="18527-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18527-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="18527-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18527-128">輸入</span><span class="sxs-lookup"><span data-stu-id="18527-128">INPUTS</span></span>

## <span data-ttu-id="18527-129">輸出</span><span class="sxs-lookup"><span data-stu-id="18527-129">OUTPUTS</span></span>

### <span data-ttu-id="18527-130">System.object</span><span class="sxs-lookup"><span data-stu-id="18527-130">System.Boolean</span></span>

## <span data-ttu-id="18527-131">筆記</span><span class="sxs-lookup"><span data-stu-id="18527-131">NOTES</span></span>

## <span data-ttu-id="18527-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="18527-132">RELATED LINKS</span></span>

