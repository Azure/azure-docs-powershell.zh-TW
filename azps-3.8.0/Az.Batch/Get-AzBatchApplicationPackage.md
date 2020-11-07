---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 17653793-3CE1-465F-87F7-20B4B8F56193
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchapplicationpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchApplicationPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchApplicationPackage.md
ms.openlocfilehash: e5e289679327b0376530f01f91310cf211465e48
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93965585"
---
# <span data-ttu-id="ebc86-101">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="ebc86-101">Get-AzBatchApplicationPackage</span></span>

## <span data-ttu-id="ebc86-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ebc86-102">SYNOPSIS</span></span>
<span data-ttu-id="ebc86-103">取得批次帳戶中應用程式套件的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ebc86-103">Gets information about an application package in a Batch account.</span></span>

## <span data-ttu-id="ebc86-104">句法</span><span class="sxs-lookup"><span data-stu-id="ebc86-104">SYNTAX</span></span>

```
Get-AzBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationName] <String>
 [[-ApplicationVersion] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ebc86-105">說明</span><span class="sxs-lookup"><span data-stu-id="ebc86-105">DESCRIPTION</span></span>
<span data-ttu-id="ebc86-106">**AzBatchApplicationPackage** Cmdlet 會取得 Azure Batch 帳戶中應用程式套件的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ebc86-106">The **Get-AzBatchApplicationPackage** cmdlet gets information about an application package in an Azure Batch account.</span></span>

## <span data-ttu-id="ebc86-107">示例</span><span class="sxs-lookup"><span data-stu-id="ebc86-107">EXAMPLES</span></span>

### <span data-ttu-id="ebc86-108">範例1：在批次帳戶中取得應用程式套件的詳細資料</span><span class="sxs-lookup"><span data-stu-id="ebc86-108">Example 1: Get details of an application package in a Batch account</span></span>
```
PS C:\>Get-AzBatchApplicationPackage -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationName "Litware" -ApplicationVersion "1.0"
Format             : zip
State              : Active
Version            : 1.0
LastActivationTime : 13/05/2016 4:03:24 AM
StorageUrl         : https://contosobatch.blob.core.windows.net/app-test
StorageUrlExpiry   : 13/05/2016 8:04:44 AM
Id                 : litware
```

<span data-ttu-id="ebc86-109">這個命令會取得 Litware 套件版本1.0 的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="ebc86-109">This command gets the details of version 1.0 of the Litware package.</span></span>

## <span data-ttu-id="ebc86-110">參數</span><span class="sxs-lookup"><span data-stu-id="ebc86-110">PARAMETERS</span></span>

### <span data-ttu-id="ebc86-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ebc86-111">-AccountName</span></span>
<span data-ttu-id="ebc86-112">指定此 Cmdlet 取得資訊的批次帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="ebc86-112">Specifies the name of the Batch account from which this cmdlet gets information.</span></span>

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

### <span data-ttu-id="ebc86-113">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="ebc86-113">-ApplicationName</span></span>
<span data-ttu-id="ebc86-114">指定應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="ebc86-114">Specifies the name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationId

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebc86-115">-ApplicationVersion</span><span class="sxs-lookup"><span data-stu-id="ebc86-115">-ApplicationVersion</span></span>
<span data-ttu-id="ebc86-116">指定應用程式的版本。</span><span class="sxs-lookup"><span data-stu-id="ebc86-116">Specifies the version of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebc86-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebc86-117">-DefaultProfile</span></span>
<span data-ttu-id="ebc86-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ebc86-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ebc86-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ebc86-119">-ResourceGroupName</span></span>
<span data-ttu-id="ebc86-120">指定包含批次帳戶之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ebc86-120">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="ebc86-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebc86-121">CommonParameters</span></span>
<span data-ttu-id="ebc86-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ebc86-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebc86-123">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ebc86-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebc86-124">輸入</span><span class="sxs-lookup"><span data-stu-id="ebc86-124">INPUTS</span></span>

### <span data-ttu-id="ebc86-125">System.object</span><span class="sxs-lookup"><span data-stu-id="ebc86-125">System.String</span></span>

## <span data-ttu-id="ebc86-126">輸出</span><span class="sxs-lookup"><span data-stu-id="ebc86-126">OUTPUTS</span></span>

### <span data-ttu-id="ebc86-127">Microsoft.Azure.Commands.Batch。PSApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="ebc86-127">Microsoft.Azure.Commands.Batch.Models.PSApplicationPackage</span></span>

## <span data-ttu-id="ebc86-128">筆記</span><span class="sxs-lookup"><span data-stu-id="ebc86-128">NOTES</span></span>

## <span data-ttu-id="ebc86-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="ebc86-129">RELATED LINKS</span></span>

[<span data-ttu-id="ebc86-130">AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="ebc86-130">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="ebc86-131">新-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="ebc86-131">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="ebc86-132">新-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="ebc86-132">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="ebc86-133">移除-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="ebc86-133">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="ebc86-134">移除-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="ebc86-134">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)

[<span data-ttu-id="ebc86-135">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="ebc86-135">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)


