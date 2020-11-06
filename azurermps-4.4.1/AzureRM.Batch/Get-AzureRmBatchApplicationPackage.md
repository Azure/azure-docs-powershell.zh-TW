---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 17653793-3CE1-465F-87F7-20B4B8F56193
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchApplicationPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchApplicationPackage.md
ms.openlocfilehash: f260af1bc26d9cf921a26e4f08c3c4feab4b79c2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449645"
---
# <span data-ttu-id="3a4b8-101">Get-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="3a4b8-101">Get-AzureRmBatchApplicationPackage</span></span>

## <span data-ttu-id="3a4b8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3a4b8-102">SYNOPSIS</span></span>
<span data-ttu-id="3a4b8-103">取得批次帳戶中應用程式套件的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="3a4b8-103">Gets information about an application package in a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3a4b8-104">句法</span><span class="sxs-lookup"><span data-stu-id="3a4b8-104">SYNTAX</span></span>

```
Get-AzureRmBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String>
 [-ApplicationId] <String> [-ApplicationVersion] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3a4b8-105">說明</span><span class="sxs-lookup"><span data-stu-id="3a4b8-105">DESCRIPTION</span></span>
<span data-ttu-id="3a4b8-106">**AzureRmBatchApplicationPackage** Cmdlet 會取得 Azure Batch 帳戶中應用程式套件的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="3a4b8-106">The **Get-AzureRmBatchApplicationPackage** cmdlet gets information about an application package in an Azure Batch account.</span></span>

## <span data-ttu-id="3a4b8-107">示例</span><span class="sxs-lookup"><span data-stu-id="3a4b8-107">EXAMPLES</span></span>

### <span data-ttu-id="3a4b8-108">範例1：在批次帳戶中取得應用程式套件的詳細資料</span><span class="sxs-lookup"><span data-stu-id="3a4b8-108">Example 1: Get details of an application package in a Batch account</span></span>
```
PS C:\>Get-AzureRmBatchApplicationPackage -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "Litware" -ApplicationVersion "1.0"
Format             : zip
State              : Active
Version            : 1.0
LastActivationTime : 13/05/2016 4:03:24 AM
StorageUrl         : https://contosobatch.blob.core.windows.net/app-test
StorageUrlExpiry   : 13/05/2016 8:04:44 AM
Id                 : litware
```

<span data-ttu-id="3a4b8-109">這個命令會取得 Litware 套件版本1.0 的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="3a4b8-109">This command gets the details of version 1.0 of the Litware package.</span></span>

## <span data-ttu-id="3a4b8-110">參數</span><span class="sxs-lookup"><span data-stu-id="3a4b8-110">PARAMETERS</span></span>

### <span data-ttu-id="3a4b8-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="3a4b8-111">-AccountName</span></span>
<span data-ttu-id="3a4b8-112">指定此 Cmdlet 取得資訊的批次帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="3a4b8-112">Specifies the name of the Batch account from which this cmdlet gets information.</span></span>

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

### <span data-ttu-id="3a4b8-113">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="3a4b8-113">-ApplicationId</span></span>
<span data-ttu-id="3a4b8-114">指定應用程式的識別碼。</span><span class="sxs-lookup"><span data-stu-id="3a4b8-114">Specifies the ID of the application.</span></span>

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

### <span data-ttu-id="3a4b8-115">-ApplicationVersion</span><span class="sxs-lookup"><span data-stu-id="3a4b8-115">-ApplicationVersion</span></span>
<span data-ttu-id="3a4b8-116">指定應用程式的版本。</span><span class="sxs-lookup"><span data-stu-id="3a4b8-116">Specifies the version of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a4b8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a4b8-117">-ResourceGroupName</span></span>
<span data-ttu-id="3a4b8-118">指定包含批次帳戶之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3a4b8-118">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="3a4b8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a4b8-119">-DefaultProfile</span></span>
<span data-ttu-id="3a4b8-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3a4b8-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3a4b8-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a4b8-121">CommonParameters</span></span>
<span data-ttu-id="3a4b8-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3a4b8-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a4b8-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3a4b8-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a4b8-124">輸入</span><span class="sxs-lookup"><span data-stu-id="3a4b8-124">INPUTS</span></span>

## <span data-ttu-id="3a4b8-125">輸出</span><span class="sxs-lookup"><span data-stu-id="3a4b8-125">OUTPUTS</span></span>

### <span data-ttu-id="3a4b8-126">Microsoft.Azure.Commands.Batch。PSApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="3a4b8-126">Microsoft.Azure.Commands.Batch.Models.PSApplicationPackage</span></span>

## <span data-ttu-id="3a4b8-127">筆記</span><span class="sxs-lookup"><span data-stu-id="3a4b8-127">NOTES</span></span>

## <span data-ttu-id="3a4b8-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="3a4b8-128">RELATED LINKS</span></span>

[<span data-ttu-id="3a4b8-129">AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="3a4b8-129">Get-AzureRmBatchApplication</span></span>](./Get-AzureRmBatchApplication.md)

[<span data-ttu-id="3a4b8-130">新-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="3a4b8-130">New-AzureRmBatchApplication</span></span>](./New-AzureRmBatchApplication.md)

[<span data-ttu-id="3a4b8-131">新-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="3a4b8-131">New-AzureRmBatchApplicationPackage</span></span>](./New-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="3a4b8-132">移除-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="3a4b8-132">Remove-AzureRmBatchApplication</span></span>](./Remove-AzureRmBatchApplication.md)

[<span data-ttu-id="3a4b8-133">移除-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="3a4b8-133">Remove-AzureRmBatchApplicationPackage</span></span>](./Remove-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="3a4b8-134">Set-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="3a4b8-134">Set-AzureRmBatchApplication</span></span>](./Set-AzureRmBatchApplication.md)

