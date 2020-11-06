---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: FD2E3442-9CEA-4390-BE9C-772C7D6FD1E2
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchapplicationpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchApplicationPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchApplicationPackage.md
ms.openlocfilehash: f4b47bb2abab783e4a6995ce57512dbd579e25e4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613632"
---
# <span data-ttu-id="e8df5-101">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="e8df5-101">Remove-AzBatchApplicationPackage</span></span>

## <span data-ttu-id="e8df5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e8df5-102">SYNOPSIS</span></span>
<span data-ttu-id="e8df5-103">刪除應用程式套件記錄和二進位檔案。</span><span class="sxs-lookup"><span data-stu-id="e8df5-103">Deletes an application package record and the binary file.</span></span>

## <span data-ttu-id="e8df5-104">句法</span><span class="sxs-lookup"><span data-stu-id="e8df5-104">SYNTAX</span></span>

```
Remove-AzBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String>
 [-ApplicationId] <String> [-ApplicationVersion] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e8df5-105">說明</span><span class="sxs-lookup"><span data-stu-id="e8df5-105">DESCRIPTION</span></span>
<span data-ttu-id="e8df5-106">**AzBatchApplicationPackage** Cmdlet 會從 Azure Batch 帳戶刪除應用程式套件記錄和二進位檔案。</span><span class="sxs-lookup"><span data-stu-id="e8df5-106">The **Remove-AzBatchApplicationPackage** cmdlet deletes an application package record and the binary file from an Azure Batch account.</span></span>

## <span data-ttu-id="e8df5-107">示例</span><span class="sxs-lookup"><span data-stu-id="e8df5-107">EXAMPLES</span></span>

### <span data-ttu-id="e8df5-108">範例1：從 Batch 帳戶刪除應用程式套件</span><span class="sxs-lookup"><span data-stu-id="e8df5-108">Example 1: Delete an application package from a Batch account</span></span>
```
PS C:\>Remove-AzBatchApplicationPackage -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "litware" -ApplicationVersion "1.0"
```

<span data-ttu-id="e8df5-109">這個命令會從 ContosoBatchGroup 帳戶刪除 Litware 應用程式的版本1.0。</span><span class="sxs-lookup"><span data-stu-id="e8df5-109">This command deletes version 1.0 of the Litware application from the ContosoBatchGroup account.</span></span>
<span data-ttu-id="e8df5-110">此命令會刪除套件記錄，以及包含套件二進位檔案的 blob。</span><span class="sxs-lookup"><span data-stu-id="e8df5-110">The command deletes both the package record and the blob that contain the package binary file.</span></span>

## <span data-ttu-id="e8df5-111">參數</span><span class="sxs-lookup"><span data-stu-id="e8df5-111">PARAMETERS</span></span>

### <span data-ttu-id="e8df5-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e8df5-112">-AccountName</span></span>
<span data-ttu-id="e8df5-113">指定此 Cmdlet 從中刪除應用程式套件的批次帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="e8df5-113">Specifies the name of the Batch account from which this cmdlet deletes an application package.</span></span>

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

### <span data-ttu-id="e8df5-114">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="e8df5-114">-ApplicationId</span></span>
<span data-ttu-id="e8df5-115">指定應用程式的識別碼。</span><span class="sxs-lookup"><span data-stu-id="e8df5-115">Specifies the ID of the application.</span></span>

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

### <span data-ttu-id="e8df5-116">-ApplicationVersion</span><span class="sxs-lookup"><span data-stu-id="e8df5-116">-ApplicationVersion</span></span>
<span data-ttu-id="e8df5-117">指定應用程式的版本。</span><span class="sxs-lookup"><span data-stu-id="e8df5-117">Specifies the version of the application.</span></span>

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

### <span data-ttu-id="e8df5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8df5-118">-DefaultProfile</span></span>
<span data-ttu-id="e8df5-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e8df5-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e8df5-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8df5-120">-ResourceGroupName</span></span>
<span data-ttu-id="e8df5-121">指定包含批次帳戶之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e8df5-121">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="e8df5-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8df5-122">CommonParameters</span></span>
<span data-ttu-id="e8df5-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e8df5-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8df5-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e8df5-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8df5-125">輸入</span><span class="sxs-lookup"><span data-stu-id="e8df5-125">INPUTS</span></span>

### <span data-ttu-id="e8df5-126">System.object</span><span class="sxs-lookup"><span data-stu-id="e8df5-126">System.String</span></span>

## <span data-ttu-id="e8df5-127">輸出</span><span class="sxs-lookup"><span data-stu-id="e8df5-127">OUTPUTS</span></span>

### <span data-ttu-id="e8df5-128">System.void</span><span class="sxs-lookup"><span data-stu-id="e8df5-128">System.Void</span></span>

## <span data-ttu-id="e8df5-129">筆記</span><span class="sxs-lookup"><span data-stu-id="e8df5-129">NOTES</span></span>

## <span data-ttu-id="e8df5-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="e8df5-130">RELATED LINKS</span></span>

[<span data-ttu-id="e8df5-131">AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="e8df5-131">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="e8df5-132">AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="e8df5-132">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="e8df5-133">新-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="e8df5-133">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="e8df5-134">新-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="e8df5-134">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="e8df5-135">移除-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="e8df5-135">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="e8df5-136">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="e8df5-136">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)

