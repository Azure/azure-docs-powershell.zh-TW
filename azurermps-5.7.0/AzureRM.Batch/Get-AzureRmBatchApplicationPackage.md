---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 17653793-3CE1-465F-87F7-20B4B8F56193
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurermbatchapplicationpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchApplicationPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchApplicationPackage.md
ms.openlocfilehash: 609c7e161b131d80f9b41355f13ced8636a591e8
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "93457676"
---
# <span data-ttu-id="3e9bf-101">Get-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="3e9bf-101">Get-AzureRmBatchApplicationPackage</span></span>

## <span data-ttu-id="3e9bf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3e9bf-102">SYNOPSIS</span></span>
<span data-ttu-id="3e9bf-103">取得批次帳戶中應用程式套件的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="3e9bf-103">Gets information about an application package in a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3e9bf-104">句法</span><span class="sxs-lookup"><span data-stu-id="3e9bf-104">SYNTAX</span></span>

```
Get-AzureRmBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String>
 [-ApplicationId] <String> [-ApplicationVersion] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3e9bf-105">說明</span><span class="sxs-lookup"><span data-stu-id="3e9bf-105">DESCRIPTION</span></span>
<span data-ttu-id="3e9bf-106">**AzureRmBatchApplicationPackage** Cmdlet 會取得 Azure Batch 帳戶中應用程式套件的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="3e9bf-106">The **Get-AzureRmBatchApplicationPackage** cmdlet gets information about an application package in an Azure Batch account.</span></span>

## <span data-ttu-id="3e9bf-107">示例</span><span class="sxs-lookup"><span data-stu-id="3e9bf-107">EXAMPLES</span></span>

### <span data-ttu-id="3e9bf-108">範例1：在批次帳戶中取得應用程式套件的詳細資料</span><span class="sxs-lookup"><span data-stu-id="3e9bf-108">Example 1: Get details of an application package in a Batch account</span></span>
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

<span data-ttu-id="3e9bf-109">這個命令會取得 Litware 套件版本1.0 的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="3e9bf-109">This command gets the details of version 1.0 of the Litware package.</span></span>

## <span data-ttu-id="3e9bf-110">參數</span><span class="sxs-lookup"><span data-stu-id="3e9bf-110">PARAMETERS</span></span>

### <span data-ttu-id="3e9bf-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="3e9bf-111">-AccountName</span></span>
<span data-ttu-id="3e9bf-112">指定此 Cmdlet 取得資訊的批次帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="3e9bf-112">Specifies the name of the Batch account from which this cmdlet gets information.</span></span>

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

### <span data-ttu-id="3e9bf-113">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="3e9bf-113">-ApplicationId</span></span>
<span data-ttu-id="3e9bf-114">指定應用程式的識別碼。</span><span class="sxs-lookup"><span data-stu-id="3e9bf-114">Specifies the ID of the application.</span></span>

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

### <span data-ttu-id="3e9bf-115">-ApplicationVersion</span><span class="sxs-lookup"><span data-stu-id="3e9bf-115">-ApplicationVersion</span></span>
<span data-ttu-id="3e9bf-116">指定應用程式的版本。</span><span class="sxs-lookup"><span data-stu-id="3e9bf-116">Specifies the version of the application.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e9bf-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e9bf-117">-DefaultProfile</span></span>
<span data-ttu-id="3e9bf-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3e9bf-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3e9bf-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e9bf-119">-ResourceGroupName</span></span>
<span data-ttu-id="3e9bf-120">指定包含批次帳戶之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3e9bf-120">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="3e9bf-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e9bf-121">CommonParameters</span></span>
<span data-ttu-id="3e9bf-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3e9bf-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e9bf-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3e9bf-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e9bf-124">輸入</span><span class="sxs-lookup"><span data-stu-id="3e9bf-124">INPUTS</span></span>

### <span data-ttu-id="3e9bf-125">所有</span><span class="sxs-lookup"><span data-stu-id="3e9bf-125">None</span></span>
<span data-ttu-id="3e9bf-126">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="3e9bf-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3e9bf-127">輸出</span><span class="sxs-lookup"><span data-stu-id="3e9bf-127">OUTPUTS</span></span>

### <span data-ttu-id="3e9bf-128">Microsoft.Azure.Commands.Batch。PSApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="3e9bf-128">Microsoft.Azure.Commands.Batch.Models.PSApplicationPackage</span></span>

## <span data-ttu-id="3e9bf-129">筆記</span><span class="sxs-lookup"><span data-stu-id="3e9bf-129">NOTES</span></span>

## <span data-ttu-id="3e9bf-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="3e9bf-130">RELATED LINKS</span></span>

[<span data-ttu-id="3e9bf-131">AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="3e9bf-131">Get-AzureRmBatchApplication</span></span>](./Get-AzureRmBatchApplication.md)

[<span data-ttu-id="3e9bf-132">新-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="3e9bf-132">New-AzureRmBatchApplication</span></span>](./New-AzureRmBatchApplication.md)

[<span data-ttu-id="3e9bf-133">新-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="3e9bf-133">New-AzureRmBatchApplicationPackage</span></span>](./New-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="3e9bf-134">移除-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="3e9bf-134">Remove-AzureRmBatchApplication</span></span>](./Remove-AzureRmBatchApplication.md)

[<span data-ttu-id="3e9bf-135">移除-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="3e9bf-135">Remove-AzureRmBatchApplicationPackage</span></span>](./Remove-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="3e9bf-136">Set-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="3e9bf-136">Set-AzureRmBatchApplication</span></span>](./Set-AzureRmBatchApplication.md)


