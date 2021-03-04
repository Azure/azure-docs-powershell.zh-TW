---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 17653793-3CE1-465F-87F7-20B4B8F56193
online version: https://docs.microsoft.com/powershell/module/az.batch/get-azbatchapplicationpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchApplicationPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchApplicationPackage.md
ms.openlocfilehash: c35630a7eda5c2174c85a5a792a03bb08ec09c1d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910777"
---
# <span data-ttu-id="dac24-101">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="dac24-101">Get-AzBatchApplicationPackage</span></span>

## <span data-ttu-id="dac24-102">簡介</span><span class="sxs-lookup"><span data-stu-id="dac24-102">SYNOPSIS</span></span>
<span data-ttu-id="dac24-103">在批次處理帳戶中，獲得應用程式套件相關資訊。</span><span class="sxs-lookup"><span data-stu-id="dac24-103">Gets information about an application package in a Batch account.</span></span>

## <span data-ttu-id="dac24-104">語法</span><span class="sxs-lookup"><span data-stu-id="dac24-104">SYNTAX</span></span>

```
Get-AzBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationName] <String>
 [[-ApplicationVersion] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dac24-105">描述</span><span class="sxs-lookup"><span data-stu-id="dac24-105">DESCRIPTION</span></span>
<span data-ttu-id="dac24-106">**Get-AzBatchApplicationPackage Cmdlet** 會取得 Azure Batch 帳戶中應用程式套件的資訊。</span><span class="sxs-lookup"><span data-stu-id="dac24-106">The **Get-AzBatchApplicationPackage** cmdlet gets information about an application package in an Azure Batch account.</span></span>

## <span data-ttu-id="dac24-107">例子</span><span class="sxs-lookup"><span data-stu-id="dac24-107">EXAMPLES</span></span>

### <span data-ttu-id="dac24-108">範例 1：取得 Batch 帳戶中的應用程式套件詳細資料</span><span class="sxs-lookup"><span data-stu-id="dac24-108">Example 1: Get details of an application package in a Batch account</span></span>
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

<span data-ttu-id="dac24-109">此命令會獲得 Litware 套件版本 1.0 的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="dac24-109">This command gets the details of version 1.0 of the Litware package.</span></span>

## <span data-ttu-id="dac24-110">參數</span><span class="sxs-lookup"><span data-stu-id="dac24-110">PARAMETERS</span></span>

### <span data-ttu-id="dac24-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="dac24-111">-AccountName</span></span>
<span data-ttu-id="dac24-112">指定此 Cmdlet 從哪個批次帳戶獲得資訊的名稱。</span><span class="sxs-lookup"><span data-stu-id="dac24-112">Specifies the name of the Batch account from which this cmdlet gets information.</span></span>

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

### <span data-ttu-id="dac24-113">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="dac24-113">-ApplicationName</span></span>
<span data-ttu-id="dac24-114">指定應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="dac24-114">Specifies the name of the application.</span></span>

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

### <span data-ttu-id="dac24-115">-ApplicationVersion</span><span class="sxs-lookup"><span data-stu-id="dac24-115">-ApplicationVersion</span></span>
<span data-ttu-id="dac24-116">指定應用程式的版本。</span><span class="sxs-lookup"><span data-stu-id="dac24-116">Specifies the version of the application.</span></span>

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

### <span data-ttu-id="dac24-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dac24-117">-DefaultProfile</span></span>
<span data-ttu-id="dac24-118">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="dac24-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dac24-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dac24-119">-ResourceGroupName</span></span>
<span data-ttu-id="dac24-120">指定包含批次帳戶的資源組名。</span><span class="sxs-lookup"><span data-stu-id="dac24-120">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="dac24-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dac24-121">CommonParameters</span></span>
<span data-ttu-id="dac24-122">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="dac24-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dac24-123">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dac24-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dac24-124">輸入</span><span class="sxs-lookup"><span data-stu-id="dac24-124">INPUTS</span></span>

### <span data-ttu-id="dac24-125">System.String</span><span class="sxs-lookup"><span data-stu-id="dac24-125">System.String</span></span>

## <span data-ttu-id="dac24-126">輸出</span><span class="sxs-lookup"><span data-stu-id="dac24-126">OUTPUTS</span></span>

### <span data-ttu-id="dac24-127">Microsoft.Azure.Commands.Batch。Models.PSApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="dac24-127">Microsoft.Azure.Commands.Batch.Models.PSApplicationPackage</span></span>

## <span data-ttu-id="dac24-128">筆記</span><span class="sxs-lookup"><span data-stu-id="dac24-128">NOTES</span></span>

## <span data-ttu-id="dac24-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="dac24-129">RELATED LINKS</span></span>

[<span data-ttu-id="dac24-130">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="dac24-130">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="dac24-131">New-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="dac24-131">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="dac24-132">New-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="dac24-132">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="dac24-133">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="dac24-133">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="dac24-134">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="dac24-134">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)

[<span data-ttu-id="dac24-135">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="dac24-135">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)


