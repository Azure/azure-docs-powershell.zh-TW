---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 2CED21D6-4BEF-423B-A04A-5B812CEB975D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurermbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureRmBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureRmBatchApplication.md
ms.openlocfilehash: df7229668547e1c018067effe50e823354d64736
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456240"
---
# <span data-ttu-id="d2e20-101">Remove-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="d2e20-101">Remove-AzureRmBatchApplication</span></span>

## <span data-ttu-id="d2e20-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d2e20-102">SYNOPSIS</span></span>
<span data-ttu-id="d2e20-103">從批次帳戶刪除應用程式。</span><span class="sxs-lookup"><span data-stu-id="d2e20-103">Deletes an application from a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d2e20-104">句法</span><span class="sxs-lookup"><span data-stu-id="d2e20-104">SYNTAX</span></span>

```
Remove-AzureRmBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d2e20-105">說明</span><span class="sxs-lookup"><span data-stu-id="d2e20-105">DESCRIPTION</span></span>
<span data-ttu-id="d2e20-106">**AzureRmBatchApplication** Cmdlet 會從 Azure Batch 帳戶刪除應用程式。</span><span class="sxs-lookup"><span data-stu-id="d2e20-106">The **Remove-AzureRmBatchApplication** cmdlet deletes an application from an Azure Batch account.</span></span>

## <span data-ttu-id="d2e20-107">示例</span><span class="sxs-lookup"><span data-stu-id="d2e20-107">EXAMPLES</span></span>

### <span data-ttu-id="d2e20-108">範例1：從批次帳戶刪除應用程式</span><span class="sxs-lookup"><span data-stu-id="d2e20-108">Example 1: Delete an application from a Batch account</span></span>
```
PS C:\>Remove-AzureRmBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "Litware"
```

<span data-ttu-id="d2e20-109">這個命令會從 ContosoBatch 帳戶刪除 Litware 應用程式。</span><span class="sxs-lookup"><span data-stu-id="d2e20-109">This command deletes the Litware application from the ContosoBatch account.</span></span>
<span data-ttu-id="d2e20-110">如果應用程式包含任何套件，命令就會失敗。</span><span class="sxs-lookup"><span data-stu-id="d2e20-110">The command fails if the application contains any packages.</span></span>

## <span data-ttu-id="d2e20-111">參數</span><span class="sxs-lookup"><span data-stu-id="d2e20-111">PARAMETERS</span></span>

### <span data-ttu-id="d2e20-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d2e20-112">-AccountName</span></span>
<span data-ttu-id="d2e20-113">指定此 Cmdlet 從中移除應用程式的批次帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="d2e20-113">Specifies the name of the Batch account from which this cmdlet removes an application.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2e20-114">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="d2e20-114">-ApplicationId</span></span>
<span data-ttu-id="d2e20-115">指定應用程式的識別碼。</span><span class="sxs-lookup"><span data-stu-id="d2e20-115">Specifies the ID of the application.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2e20-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2e20-116">-DefaultProfile</span></span>
<span data-ttu-id="d2e20-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d2e20-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d2e20-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2e20-118">-ResourceGroupName</span></span>
<span data-ttu-id="d2e20-119">指定包含批次帳戶之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d2e20-119">Specifies the name of the resource group that contains the Batch account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2e20-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2e20-120">CommonParameters</span></span>
<span data-ttu-id="d2e20-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d2e20-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2e20-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d2e20-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2e20-123">輸入</span><span class="sxs-lookup"><span data-stu-id="d2e20-123">INPUTS</span></span>

### <span data-ttu-id="d2e20-124">所有</span><span class="sxs-lookup"><span data-stu-id="d2e20-124">None</span></span>
<span data-ttu-id="d2e20-125">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="d2e20-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d2e20-126">輸出</span><span class="sxs-lookup"><span data-stu-id="d2e20-126">OUTPUTS</span></span>

## <span data-ttu-id="d2e20-127">筆記</span><span class="sxs-lookup"><span data-stu-id="d2e20-127">NOTES</span></span>

## <span data-ttu-id="d2e20-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="d2e20-128">RELATED LINKS</span></span>

[<span data-ttu-id="d2e20-129">AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="d2e20-129">Get-AzureRmBatchApplication</span></span>](./Get-AzureRmBatchApplication.md)

[<span data-ttu-id="d2e20-130">AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="d2e20-130">Get-AzureRmBatchApplicationPackage</span></span>](./Get-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="d2e20-131">新-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="d2e20-131">New-AzureRmBatchApplication</span></span>](./New-AzureRmBatchApplication.md)

[<span data-ttu-id="d2e20-132">新-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="d2e20-132">New-AzureRmBatchApplicationPackage</span></span>](./New-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="d2e20-133">移除-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="d2e20-133">Remove-AzureRmBatchApplicationPackage</span></span>](./Remove-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="d2e20-134">Set-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="d2e20-134">Set-AzureRmBatchApplication</span></span>](./Set-AzureRmBatchApplication.md)


