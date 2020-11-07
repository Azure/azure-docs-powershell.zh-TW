---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: 4D64CA4D-1066-4D3E-9317-60D37D9DE2BB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.media/new-azurermmediaservicestorageconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/New-AzureRmMediaServiceStorageConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/New-AzureRmMediaServiceStorageConfig.md
ms.openlocfilehash: efc157e2e4395055d1af2ef80f0a9fcc98886d15
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626084"
---
# <span data-ttu-id="d2bdb-101">New-AzureRmMediaServiceStorageConfig</span><span class="sxs-lookup"><span data-stu-id="d2bdb-101">New-AzureRmMediaServiceStorageConfig</span></span>

## <span data-ttu-id="d2bdb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d2bdb-102">SYNOPSIS</span></span>
<span data-ttu-id="d2bdb-103">為媒體服務 Cmdlet 建立儲存帳戶設定。</span><span class="sxs-lookup"><span data-stu-id="d2bdb-103">Create a storage account configuration for the media service cmdlets.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d2bdb-104">句法</span><span class="sxs-lookup"><span data-stu-id="d2bdb-104">SYNTAX</span></span>

```
New-AzureRmMediaServiceStorageConfig [-DefaultProfile <IAzureContextContainer>] [-StorageAccountId] <String>
 [-IsPrimary] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2bdb-105">說明</span><span class="sxs-lookup"><span data-stu-id="d2bdb-105">DESCRIPTION</span></span>
<span data-ttu-id="d2bdb-106">**新的 AzureRmMediaServiceStorageConfig** Cmdlet 會建立媒體服務 Cmdlet 的儲存帳戶配置。</span><span class="sxs-lookup"><span data-stu-id="d2bdb-106">The **New-AzureRmMediaServiceStorageConfig** cmdlet creates a storage account configuration for the media service cmdlets.</span></span>

## <span data-ttu-id="d2bdb-107">示例</span><span class="sxs-lookup"><span data-stu-id="d2bdb-107">EXAMPLES</span></span>

### <span data-ttu-id="d2bdb-108">範例1：建立媒體服務 Cmdlet 的儲存帳戶設定</span><span class="sxs-lookup"><span data-stu-id="d2bdb-108">Example 1: Create a storage account configuration for the media service cmdlets</span></span>
```
PS C:\>
$StorageAccount = New-AzureRmStorageAccount -ResourceGroupName $ResourceGroupName -Name "Storage1" -Location "East US" -Type "Standard_GRS"

PS C:\> New-AzureRmMediaServiceStorageConfig -StorageAccountId $StorageAccount.Id -IsPrimary
```

<span data-ttu-id="d2bdb-109">第一個命令會使用 **AzureRmStorageAccount** Cmdlet 建立儲存空間帳戶物件。</span><span class="sxs-lookup"><span data-stu-id="d2bdb-109">The first command creates a storage account object by using **the New-AzureRmStorageAccount** cmdlet.</span></span>
<span data-ttu-id="d2bdb-110">命令會將此儲存帳戶 Storage1 及類型命名為 Standard_GRS，並將結果儲存在名為 $StorageAccount 的變數中。</span><span class="sxs-lookup"><span data-stu-id="d2bdb-110">The command names this storage account Storage1 and the type is named Standard_GRS and stores the result in the variable named $StorageAccount.</span></span>
<span data-ttu-id="d2bdb-111">第二個命令會使用儲存在 $StorageAccount 變數中的儲存空間帳戶識別碼資訊，來建立儲存設定物件，作為與媒體服務相關聯的主要儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="d2bdb-111">The second command creates a storage configuration object as the primary storage account associated with the media service using the storage account ID information stored in the $StorageAccount variable.</span></span>

## <span data-ttu-id="d2bdb-112">參數</span><span class="sxs-lookup"><span data-stu-id="d2bdb-112">PARAMETERS</span></span>

### <span data-ttu-id="d2bdb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2bdb-113">-DefaultProfile</span></span>
<span data-ttu-id="d2bdb-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="d2bdb-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d2bdb-115">-IsPrimary</span><span class="sxs-lookup"><span data-stu-id="d2bdb-115">-IsPrimary</span></span>
<span data-ttu-id="d2bdb-116">表示 Cmdlet 會建立儲存空間帳戶做為媒體服務的主要儲存空間。</span><span class="sxs-lookup"><span data-stu-id="d2bdb-116">Indicates that the cmdlet creates the storage account as the primary storage for the media service.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2bdb-117">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="d2bdb-117">-StorageAccountId</span></span>
<span data-ttu-id="d2bdb-118">指定儲存空間帳戶的 ID。</span><span class="sxs-lookup"><span data-stu-id="d2bdb-118">Specifies the ID of the storage account.</span></span>

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

### <span data-ttu-id="d2bdb-119">-確認</span><span class="sxs-lookup"><span data-stu-id="d2bdb-119">-Confirm</span></span>
<span data-ttu-id="d2bdb-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d2bdb-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2bdb-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2bdb-121">-WhatIf</span></span>
<span data-ttu-id="d2bdb-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d2bdb-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2bdb-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d2bdb-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2bdb-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2bdb-124">CommonParameters</span></span>
<span data-ttu-id="d2bdb-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d2bdb-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2bdb-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d2bdb-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2bdb-127">輸入</span><span class="sxs-lookup"><span data-stu-id="d2bdb-127">INPUTS</span></span>

### <span data-ttu-id="d2bdb-128">System.object</span><span class="sxs-lookup"><span data-stu-id="d2bdb-128">System.String</span></span>

## <span data-ttu-id="d2bdb-129">輸出</span><span class="sxs-lookup"><span data-stu-id="d2bdb-129">OUTPUTS</span></span>

### <span data-ttu-id="d2bdb-130">PSStorageAccount 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="d2bdb-130">Microsoft.Azure.Commands.Media.Models.PSStorageAccount</span></span>

## <span data-ttu-id="d2bdb-131">筆記</span><span class="sxs-lookup"><span data-stu-id="d2bdb-131">NOTES</span></span>

## <span data-ttu-id="d2bdb-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="d2bdb-132">RELATED LINKS</span></span>

[<span data-ttu-id="d2bdb-133">同步處理-AzureRmMediaServiceStorageKeys</span><span class="sxs-lookup"><span data-stu-id="d2bdb-133">Sync-AzureRmMediaServiceStorageKeys</span></span>](./Sync-AzureRmMediaServiceStorageKeys.md)


