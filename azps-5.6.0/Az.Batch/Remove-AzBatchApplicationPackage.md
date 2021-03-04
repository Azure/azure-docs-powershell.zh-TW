---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: FD2E3442-9CEA-4390-BE9C-772C7D6FD1E2
online version: https://docs.microsoft.com/powershell/module/az.batch/remove-azbatchapplicationpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchApplicationPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchApplicationPackage.md
ms.openlocfilehash: 7c51776683d4a8ecb777fd56d8b83ca4ae672206
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906345"
---
# <span data-ttu-id="50b44-101">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="50b44-101">Remove-AzBatchApplicationPackage</span></span>

## <span data-ttu-id="50b44-102">簡介</span><span class="sxs-lookup"><span data-stu-id="50b44-102">SYNOPSIS</span></span>
<span data-ttu-id="50b44-103">刪除應用程式套件記錄和二進位檔案。</span><span class="sxs-lookup"><span data-stu-id="50b44-103">Deletes an application package record and the binary file.</span></span>

## <span data-ttu-id="50b44-104">語法</span><span class="sxs-lookup"><span data-stu-id="50b44-104">SYNTAX</span></span>

```
Remove-AzBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String>
 [-ApplicationName] <String> [-ApplicationVersion] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="50b44-105">描述</span><span class="sxs-lookup"><span data-stu-id="50b44-105">DESCRIPTION</span></span>
<span data-ttu-id="50b44-106">**Remove-AzBatchApplicationPackage Cmdlet** 會從 Azure Batch 帳戶刪除應用程式套件記錄和二進位檔案。</span><span class="sxs-lookup"><span data-stu-id="50b44-106">The **Remove-AzBatchApplicationPackage** cmdlet deletes an application package record and the binary file from an Azure Batch account.</span></span>

## <span data-ttu-id="50b44-107">例子</span><span class="sxs-lookup"><span data-stu-id="50b44-107">EXAMPLES</span></span>

### <span data-ttu-id="50b44-108">範例 1：從 Batch 帳戶刪除應用程式套件</span><span class="sxs-lookup"><span data-stu-id="50b44-108">Example 1: Delete an application package from a Batch account</span></span>
```
PS C:\>Remove-AzBatchApplicationPackage -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationName "litware" -ApplicationVersion "1.0"
```

<span data-ttu-id="50b44-109">此命令會從 ContosoBatchGroup 帳戶刪除 Litware 應用程式的版本 1.0。</span><span class="sxs-lookup"><span data-stu-id="50b44-109">This command deletes version 1.0 of the Litware application from the ContosoBatchGroup account.</span></span>
<span data-ttu-id="50b44-110">該命令會同時刪除套件記錄和包含套件二進位檔案的 Blob。</span><span class="sxs-lookup"><span data-stu-id="50b44-110">The command deletes both the package record and the blob that contain the package binary file.</span></span>

## <span data-ttu-id="50b44-111">參數</span><span class="sxs-lookup"><span data-stu-id="50b44-111">PARAMETERS</span></span>

### <span data-ttu-id="50b44-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="50b44-112">-AccountName</span></span>
<span data-ttu-id="50b44-113">指定此 Cmdlet 刪除應用程式套件的批次帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="50b44-113">Specifies the name of the Batch account from which this cmdlet deletes an application package.</span></span>

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

### <span data-ttu-id="50b44-114">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="50b44-114">-ApplicationName</span></span>
<span data-ttu-id="50b44-115">指定應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="50b44-115">Specifies the name of the application.</span></span>

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

### <span data-ttu-id="50b44-116">-ApplicationVersion</span><span class="sxs-lookup"><span data-stu-id="50b44-116">-ApplicationVersion</span></span>
<span data-ttu-id="50b44-117">指定應用程式的版本。</span><span class="sxs-lookup"><span data-stu-id="50b44-117">Specifies the version of the application.</span></span>

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

### <span data-ttu-id="50b44-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50b44-118">-DefaultProfile</span></span>
<span data-ttu-id="50b44-119">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="50b44-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="50b44-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50b44-120">-ResourceGroupName</span></span>
<span data-ttu-id="50b44-121">指定包含批次帳戶的資源組名。</span><span class="sxs-lookup"><span data-stu-id="50b44-121">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="50b44-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50b44-122">CommonParameters</span></span>
<span data-ttu-id="50b44-123">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="50b44-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50b44-124">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="50b44-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50b44-125">輸入</span><span class="sxs-lookup"><span data-stu-id="50b44-125">INPUTS</span></span>

### <span data-ttu-id="50b44-126">System.String</span><span class="sxs-lookup"><span data-stu-id="50b44-126">System.String</span></span>

## <span data-ttu-id="50b44-127">輸出</span><span class="sxs-lookup"><span data-stu-id="50b44-127">OUTPUTS</span></span>

### <span data-ttu-id="50b44-128">System.Void</span><span class="sxs-lookup"><span data-stu-id="50b44-128">System.Void</span></span>

## <span data-ttu-id="50b44-129">筆記</span><span class="sxs-lookup"><span data-stu-id="50b44-129">NOTES</span></span>

## <span data-ttu-id="50b44-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="50b44-130">RELATED LINKS</span></span>

[<span data-ttu-id="50b44-131">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="50b44-131">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="50b44-132">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="50b44-132">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="50b44-133">New-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="50b44-133">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="50b44-134">New-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="50b44-134">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="50b44-135">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="50b44-135">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="50b44-136">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="50b44-136">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)


