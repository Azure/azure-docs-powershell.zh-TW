---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: FF111B74-90A3-4F7C-B515-CE1EEF68EB54
online version: https://docs.microsoft.com/powershell/module/az.batch/new-azbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchApplication.md
ms.openlocfilehash: e22c1ef6a95fafe21f0fd10a47a67098976395e5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905609"
---
# <span data-ttu-id="a6bd3-101">New-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="a6bd3-101">New-AzBatchApplication</span></span>

## <span data-ttu-id="a6bd3-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a6bd3-102">SYNOPSIS</span></span>
<span data-ttu-id="a6bd3-103">新增應用程式至指定的批次帳戶。</span><span class="sxs-lookup"><span data-stu-id="a6bd3-103">Adds an application to the specified Batch account.</span></span>

## <span data-ttu-id="a6bd3-104">語法</span><span class="sxs-lookup"><span data-stu-id="a6bd3-104">SYNTAX</span></span>

```
New-AzBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationName] <String>
 [[-AllowUpdates] <Boolean>] [[-DisplayName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a6bd3-105">描述</span><span class="sxs-lookup"><span data-stu-id="a6bd3-105">DESCRIPTION</span></span>
<span data-ttu-id="a6bd3-106">**New-AzBatchApplication** Cmdlet 會將應用程式新增到指定的 Azure Batch 帳戶。</span><span class="sxs-lookup"><span data-stu-id="a6bd3-106">The **New-AzBatchApplication** cmdlet adds an application to the specified Azure Batch account.</span></span>

## <span data-ttu-id="a6bd3-107">例子</span><span class="sxs-lookup"><span data-stu-id="a6bd3-107">EXAMPLES</span></span>

### <span data-ttu-id="a6bd3-108">範例 1：新增空白應用程式至 Batch 帳戶</span><span class="sxs-lookup"><span data-stu-id="a6bd3-108">Example 1: Add an empty application to a Batch account</span></span>
```
PS C:\>New-AzBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationName "Litware" -AllowUpdates $True -DisplayName "Litware Advanced Reticulator"
```

<span data-ttu-id="a6bd3-109">此命令在 ContosoBatch 帳戶中建立 Litware 應用程式。</span><span class="sxs-lookup"><span data-stu-id="a6bd3-109">This command creates the Litware application in the ContosoBatch account.</span></span>
<span data-ttu-id="a6bd3-110">應用程式一開始不包含任何套件。</span><span class="sxs-lookup"><span data-stu-id="a6bd3-110">The application initially contains no packages.</span></span>

## <span data-ttu-id="a6bd3-111">參數</span><span class="sxs-lookup"><span data-stu-id="a6bd3-111">PARAMETERS</span></span>

### <span data-ttu-id="a6bd3-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a6bd3-112">-AccountName</span></span>
<span data-ttu-id="a6bd3-113">指定此 Cmdlet 新增應用程式的 Batch 帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="a6bd3-113">Specifies the name of the Batch account to which this cmdlet adds an application.</span></span>

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

### <span data-ttu-id="a6bd3-114">-AllowUpdates</span><span class="sxs-lookup"><span data-stu-id="a6bd3-114">-AllowUpdates</span></span>
<span data-ttu-id="a6bd3-115">指定是否可以使用相同的版本字串來覆蓋應用程式內的套件。</span><span class="sxs-lookup"><span data-stu-id="a6bd3-115">Specifies whether packages within the application can be overwritten using the same version string.</span></span>

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

### <span data-ttu-id="a6bd3-116">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="a6bd3-116">-ApplicationName</span></span>
<span data-ttu-id="a6bd3-117">指定應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="a6bd3-117">Specifies the name of the application.</span></span>

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

### <span data-ttu-id="a6bd3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6bd3-118">-DefaultProfile</span></span>
<span data-ttu-id="a6bd3-119">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a6bd3-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a6bd3-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="a6bd3-120">-DisplayName</span></span>
<span data-ttu-id="a6bd3-121">指定應用程式的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="a6bd3-121">Specifies the display name for the application.</span></span>

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

### <span data-ttu-id="a6bd3-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6bd3-122">-ResourceGroupName</span></span>
<span data-ttu-id="a6bd3-123">指定包含批次帳戶的資源組名。</span><span class="sxs-lookup"><span data-stu-id="a6bd3-123">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="a6bd3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6bd3-124">CommonParameters</span></span>
<span data-ttu-id="a6bd3-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a6bd3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6bd3-126">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a6bd3-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6bd3-127">輸入</span><span class="sxs-lookup"><span data-stu-id="a6bd3-127">INPUTS</span></span>

### <span data-ttu-id="a6bd3-128">System.String</span><span class="sxs-lookup"><span data-stu-id="a6bd3-128">System.String</span></span>

### <span data-ttu-id="a6bd3-129">System.Nullable'1[[System.Boolean， mscorlib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="a6bd3-129">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="a6bd3-130">輸出</span><span class="sxs-lookup"><span data-stu-id="a6bd3-130">OUTPUTS</span></span>

### <span data-ttu-id="a6bd3-131">Microsoft.Azure.Commands.Batch。Models.PSApplication</span><span class="sxs-lookup"><span data-stu-id="a6bd3-131">Microsoft.Azure.Commands.Batch.Models.PSApplication</span></span>

## <span data-ttu-id="a6bd3-132">筆記</span><span class="sxs-lookup"><span data-stu-id="a6bd3-132">NOTES</span></span>

## <span data-ttu-id="a6bd3-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="a6bd3-133">RELATED LINKS</span></span>

[<span data-ttu-id="a6bd3-134">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="a6bd3-134">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="a6bd3-135">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="a6bd3-135">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="a6bd3-136">New-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="a6bd3-136">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="a6bd3-137">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="a6bd3-137">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="a6bd3-138">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="a6bd3-138">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)

[<span data-ttu-id="a6bd3-139">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="a6bd3-139">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)


