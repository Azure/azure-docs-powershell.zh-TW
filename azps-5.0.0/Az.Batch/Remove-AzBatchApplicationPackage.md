---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: FD2E3442-9CEA-4390-BE9C-772C7D6FD1E2
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchapplicationpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchApplicationPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchApplicationPackage.md
ms.openlocfilehash: f88994649281d442f37a2bafa2cf2b4f74e6b86e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94138519"
---
# <span data-ttu-id="080fd-101">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="080fd-101">Remove-AzBatchApplicationPackage</span></span>

## <span data-ttu-id="080fd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="080fd-102">SYNOPSIS</span></span>
<span data-ttu-id="080fd-103">刪除應用程式套件記錄和二進位檔案。</span><span class="sxs-lookup"><span data-stu-id="080fd-103">Deletes an application package record and the binary file.</span></span>

## <span data-ttu-id="080fd-104">句法</span><span class="sxs-lookup"><span data-stu-id="080fd-104">SYNTAX</span></span>

```
Remove-AzBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String>
 [-ApplicationName] <String> [-ApplicationVersion] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="080fd-105">說明</span><span class="sxs-lookup"><span data-stu-id="080fd-105">DESCRIPTION</span></span>
<span data-ttu-id="080fd-106">**AzBatchApplicationPackage** Cmdlet 會從 Azure Batch 帳戶刪除應用程式套件記錄和二進位檔案。</span><span class="sxs-lookup"><span data-stu-id="080fd-106">The **Remove-AzBatchApplicationPackage** cmdlet deletes an application package record and the binary file from an Azure Batch account.</span></span>

## <span data-ttu-id="080fd-107">示例</span><span class="sxs-lookup"><span data-stu-id="080fd-107">EXAMPLES</span></span>

### <span data-ttu-id="080fd-108">範例1：從 Batch 帳戶刪除應用程式套件</span><span class="sxs-lookup"><span data-stu-id="080fd-108">Example 1: Delete an application package from a Batch account</span></span>
```
PS C:\>Remove-AzBatchApplicationPackage -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationName "litware" -ApplicationVersion "1.0"
```

<span data-ttu-id="080fd-109">這個命令會從 ContosoBatchGroup 帳戶刪除 Litware 應用程式的版本1.0。</span><span class="sxs-lookup"><span data-stu-id="080fd-109">This command deletes version 1.0 of the Litware application from the ContosoBatchGroup account.</span></span>
<span data-ttu-id="080fd-110">此命令會刪除套件記錄，以及包含套件二進位檔案的 blob。</span><span class="sxs-lookup"><span data-stu-id="080fd-110">The command deletes both the package record and the blob that contain the package binary file.</span></span>

## <span data-ttu-id="080fd-111">參數</span><span class="sxs-lookup"><span data-stu-id="080fd-111">PARAMETERS</span></span>

### <span data-ttu-id="080fd-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="080fd-112">-AccountName</span></span>
<span data-ttu-id="080fd-113">指定此 Cmdlet 從中刪除應用程式套件的批次帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="080fd-113">Specifies the name of the Batch account from which this cmdlet deletes an application package.</span></span>

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

### <span data-ttu-id="080fd-114">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="080fd-114">-ApplicationName</span></span>
<span data-ttu-id="080fd-115">指定應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="080fd-115">Specifies the name of the application.</span></span>

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

### <span data-ttu-id="080fd-116">-ApplicationVersion</span><span class="sxs-lookup"><span data-stu-id="080fd-116">-ApplicationVersion</span></span>
<span data-ttu-id="080fd-117">指定應用程式的版本。</span><span class="sxs-lookup"><span data-stu-id="080fd-117">Specifies the version of the application.</span></span>

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

### <span data-ttu-id="080fd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="080fd-118">-DefaultProfile</span></span>
<span data-ttu-id="080fd-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="080fd-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="080fd-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="080fd-120">-ResourceGroupName</span></span>
<span data-ttu-id="080fd-121">指定包含批次帳戶之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="080fd-121">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="080fd-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="080fd-122">CommonParameters</span></span>
<span data-ttu-id="080fd-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="080fd-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="080fd-124">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="080fd-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="080fd-125">輸入</span><span class="sxs-lookup"><span data-stu-id="080fd-125">INPUTS</span></span>

### <span data-ttu-id="080fd-126">System.object</span><span class="sxs-lookup"><span data-stu-id="080fd-126">System.String</span></span>

## <span data-ttu-id="080fd-127">輸出</span><span class="sxs-lookup"><span data-stu-id="080fd-127">OUTPUTS</span></span>

### <span data-ttu-id="080fd-128">System.void</span><span class="sxs-lookup"><span data-stu-id="080fd-128">System.Void</span></span>

## <span data-ttu-id="080fd-129">筆記</span><span class="sxs-lookup"><span data-stu-id="080fd-129">NOTES</span></span>

## <span data-ttu-id="080fd-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="080fd-130">RELATED LINKS</span></span>

[<span data-ttu-id="080fd-131">AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="080fd-131">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="080fd-132">AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="080fd-132">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="080fd-133">新-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="080fd-133">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="080fd-134">新-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="080fd-134">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="080fd-135">移除-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="080fd-135">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="080fd-136">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="080fd-136">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)

