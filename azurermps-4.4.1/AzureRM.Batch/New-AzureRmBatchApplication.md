---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: FF111B74-90A3-4F7C-B515-CE1EEF68EB54
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchApplication.md
ms.openlocfilehash: 6c2ab80f5b9fb38ed2f6399d9f186134f4659edf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450864"
---
# <span data-ttu-id="b27a5-101">New-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="b27a5-101">New-AzureRmBatchApplication</span></span>

## <span data-ttu-id="b27a5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b27a5-102">SYNOPSIS</span></span>
<span data-ttu-id="b27a5-103">將應用程式新增至指定的批次帳戶。</span><span class="sxs-lookup"><span data-stu-id="b27a5-103">Adds an application to the specified Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b27a5-104">句法</span><span class="sxs-lookup"><span data-stu-id="b27a5-104">SYNTAX</span></span>

```
New-AzureRmBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationId] <String>
 [[-AllowUpdates] <Boolean>] [[-DisplayName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b27a5-105">說明</span><span class="sxs-lookup"><span data-stu-id="b27a5-105">DESCRIPTION</span></span>
<span data-ttu-id="b27a5-106">**新的-AzureRmBatchApplication** Cmdlet 會將應用程式新增至指定的 Azure Batch 帳戶。</span><span class="sxs-lookup"><span data-stu-id="b27a5-106">The **New-AzureRmBatchApplication** cmdlet adds an application to the specified Azure Batch account.</span></span>

## <span data-ttu-id="b27a5-107">示例</span><span class="sxs-lookup"><span data-stu-id="b27a5-107">EXAMPLES</span></span>

### <span data-ttu-id="b27a5-108">範例1：在批次帳戶中新增空白的應用程式</span><span class="sxs-lookup"><span data-stu-id="b27a5-108">Example 1: Add an empty application to a Batch account</span></span>
```
PS C:\>New-AzureRmBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "Litware" -AllowUpdates $True -DisplayName "Litware Advanced Reticulator"
```

<span data-ttu-id="b27a5-109">這個命令會在 ContosoBatch 帳戶中建立 Litware 應用程式。</span><span class="sxs-lookup"><span data-stu-id="b27a5-109">This command creates the Litware application in the ContosoBatch account.</span></span>
<span data-ttu-id="b27a5-110">應用程式最初不會包含任何套件。</span><span class="sxs-lookup"><span data-stu-id="b27a5-110">The application initially contains no packages.</span></span>

## <span data-ttu-id="b27a5-111">參數</span><span class="sxs-lookup"><span data-stu-id="b27a5-111">PARAMETERS</span></span>

### <span data-ttu-id="b27a5-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b27a5-112">-AccountName</span></span>
<span data-ttu-id="b27a5-113">指定此 Cmdlet 要新增應用程式的批次帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="b27a5-113">Specifies the name of the Batch account to which this cmdlet adds an application.</span></span>

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

### <span data-ttu-id="b27a5-114">-AllowUpdates</span><span class="sxs-lookup"><span data-stu-id="b27a5-114">-AllowUpdates</span></span>
<span data-ttu-id="b27a5-115">指定是否可使用相同的版本字串來覆寫應用程式中的套件。</span><span class="sxs-lookup"><span data-stu-id="b27a5-115">Specifies whether packages within the application can be overwritten using the same version string.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b27a5-116">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="b27a5-116">-ApplicationId</span></span>
<span data-ttu-id="b27a5-117">指定應用程式的識別碼。</span><span class="sxs-lookup"><span data-stu-id="b27a5-117">Specifies the ID of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b27a5-118">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="b27a5-118">-DisplayName</span></span>
<span data-ttu-id="b27a5-119">指定應用程式的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="b27a5-119">Specifies the display name for the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b27a5-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b27a5-120">-ResourceGroupName</span></span>
<span data-ttu-id="b27a5-121">指定包含批次帳戶之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b27a5-121">Specifies the name of the resource group that contains the Batch account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b27a5-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b27a5-122">-DefaultProfile</span></span>
<span data-ttu-id="b27a5-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b27a5-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b27a5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b27a5-124">CommonParameters</span></span>
<span data-ttu-id="b27a5-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b27a5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b27a5-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b27a5-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b27a5-127">輸入</span><span class="sxs-lookup"><span data-stu-id="b27a5-127">INPUTS</span></span>

## <span data-ttu-id="b27a5-128">輸出</span><span class="sxs-lookup"><span data-stu-id="b27a5-128">OUTPUTS</span></span>

### <span data-ttu-id="b27a5-129">Microsoft.Azure.Commands.Batch。PSApplication</span><span class="sxs-lookup"><span data-stu-id="b27a5-129">Microsoft.Azure.Commands.Batch.Models.PSApplication</span></span>

## <span data-ttu-id="b27a5-130">筆記</span><span class="sxs-lookup"><span data-stu-id="b27a5-130">NOTES</span></span>

## <span data-ttu-id="b27a5-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="b27a5-131">RELATED LINKS</span></span>

[<span data-ttu-id="b27a5-132">AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="b27a5-132">Get-AzureRmBatchApplication</span></span>](./Get-AzureRmBatchApplication.md)

[<span data-ttu-id="b27a5-133">AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="b27a5-133">Get-AzureRmBatchApplicationPackage</span></span>](./Get-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="b27a5-134">新-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="b27a5-134">New-AzureRmBatchApplicationPackage</span></span>](./New-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="b27a5-135">移除-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="b27a5-135">Remove-AzureRmBatchApplication</span></span>](./Remove-AzureRmBatchApplication.md)

[<span data-ttu-id="b27a5-136">移除-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="b27a5-136">Remove-AzureRmBatchApplicationPackage</span></span>](./Remove-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="b27a5-137">Set-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="b27a5-137">Set-AzureRmBatchApplication</span></span>](./Set-AzureRmBatchApplication.md)


