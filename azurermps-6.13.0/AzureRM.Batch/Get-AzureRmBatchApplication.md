---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: CF8B8E94-3C6C-4D68-B55B-956393890946
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurermbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchApplication.md
ms.openlocfilehash: 2a1096d4424ff920c84c8fe7a2a4704496f95dfb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445736"
---
# <span data-ttu-id="1b6df-101">Get-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="1b6df-101">Get-AzureRmBatchApplication</span></span>

## <span data-ttu-id="1b6df-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1b6df-102">SYNOPSIS</span></span>
<span data-ttu-id="1b6df-103">取得特定應用程式的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="1b6df-103">Gets information about the specified application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1b6df-104">句法</span><span class="sxs-lookup"><span data-stu-id="1b6df-104">SYNTAX</span></span>

```
Get-AzureRmBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [[-ApplicationId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1b6df-105">說明</span><span class="sxs-lookup"><span data-stu-id="1b6df-105">DESCRIPTION</span></span>
<span data-ttu-id="1b6df-106">**AzureRmBatchApplication** Cmdlet 會取得 Azure Batch 帳戶中應用程式的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="1b6df-106">The **Get-AzureRmBatchApplication** cmdlet gets information about an application in an Azure Batch account.</span></span>

## <span data-ttu-id="1b6df-107">示例</span><span class="sxs-lookup"><span data-stu-id="1b6df-107">EXAMPLES</span></span>

### <span data-ttu-id="1b6df-108">範例1：以批次帳戶顯示應用程式</span><span class="sxs-lookup"><span data-stu-id="1b6df-108">Example 1: Display the applications in a Batch account</span></span>
```
PS C:\>Get-AzureRmBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup"
ApplicationId AllowUpdates DisplayName

------------- ------------ ----------------------------

litware       False        Litware Advanced Reticulator
```

<span data-ttu-id="1b6df-109">這個命令會顯示 ContosoBatch 帳戶中的所有應用程式。</span><span class="sxs-lookup"><span data-stu-id="1b6df-109">This command displays all applications in the ContosoBatch account.</span></span>

## <span data-ttu-id="1b6df-110">參數</span><span class="sxs-lookup"><span data-stu-id="1b6df-110">PARAMETERS</span></span>

### <span data-ttu-id="1b6df-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1b6df-111">-AccountName</span></span>
<span data-ttu-id="1b6df-112">指定包含應用程式的批次帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="1b6df-112">Specifies the name of the Batch account that contains the application.</span></span>

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

### <span data-ttu-id="1b6df-113">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="1b6df-113">-ApplicationId</span></span>
<span data-ttu-id="1b6df-114">指定應用程式的識別碼。</span><span class="sxs-lookup"><span data-stu-id="1b6df-114">Specifies the ID of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b6df-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b6df-115">-DefaultProfile</span></span>
<span data-ttu-id="1b6df-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1b6df-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1b6df-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b6df-117">-ResourceGroupName</span></span>
<span data-ttu-id="1b6df-118">指定包含批次帳戶之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1b6df-118">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="1b6df-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b6df-119">CommonParameters</span></span>
<span data-ttu-id="1b6df-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1b6df-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b6df-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1b6df-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b6df-122">輸入</span><span class="sxs-lookup"><span data-stu-id="1b6df-122">INPUTS</span></span>

### <span data-ttu-id="1b6df-123">System.object</span><span class="sxs-lookup"><span data-stu-id="1b6df-123">System.String</span></span>

## <span data-ttu-id="1b6df-124">輸出</span><span class="sxs-lookup"><span data-stu-id="1b6df-124">OUTPUTS</span></span>

### <span data-ttu-id="1b6df-125">Microsoft.Azure.Commands.Batch。PSApplication</span><span class="sxs-lookup"><span data-stu-id="1b6df-125">Microsoft.Azure.Commands.Batch.Models.PSApplication</span></span>

## <span data-ttu-id="1b6df-126">筆記</span><span class="sxs-lookup"><span data-stu-id="1b6df-126">NOTES</span></span>

## <span data-ttu-id="1b6df-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="1b6df-127">RELATED LINKS</span></span>

[<span data-ttu-id="1b6df-128">AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="1b6df-128">Get-AzureRmBatchApplicationPackage</span></span>](./Get-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="1b6df-129">新-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="1b6df-129">New-AzureRmBatchApplication</span></span>](./New-AzureRmBatchApplication.md)

[<span data-ttu-id="1b6df-130">新-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="1b6df-130">New-AzureRmBatchApplicationPackage</span></span>](./New-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="1b6df-131">移除-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="1b6df-131">Remove-AzureRmBatchApplication</span></span>](./Remove-AzureRmBatchApplication.md)

[<span data-ttu-id="1b6df-132">移除-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="1b6df-132">Remove-AzureRmBatchApplicationPackage</span></span>](./Remove-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="1b6df-133">Set-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="1b6df-133">Set-AzureRmBatchApplication</span></span>](./Set-AzureRmBatchApplication.md)


