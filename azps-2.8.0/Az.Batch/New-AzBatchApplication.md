---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: FF111B74-90A3-4F7C-B515-CE1EEF68EB54
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchApplication.md
ms.openlocfilehash: 0c1d847045cc4fb8be39674c13c38114ee9d3a57
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613637"
---
# <span data-ttu-id="c3ac8-101">New-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="c3ac8-101">New-AzBatchApplication</span></span>

## <span data-ttu-id="c3ac8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c3ac8-102">SYNOPSIS</span></span>
<span data-ttu-id="c3ac8-103">將應用程式新增至指定的批次帳戶。</span><span class="sxs-lookup"><span data-stu-id="c3ac8-103">Adds an application to the specified Batch account.</span></span>

## <span data-ttu-id="c3ac8-104">句法</span><span class="sxs-lookup"><span data-stu-id="c3ac8-104">SYNTAX</span></span>

```
New-AzBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationId] <String>
 [[-AllowUpdates] <Boolean>] [[-DisplayName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c3ac8-105">說明</span><span class="sxs-lookup"><span data-stu-id="c3ac8-105">DESCRIPTION</span></span>
<span data-ttu-id="c3ac8-106">**新的-AzBatchApplication** Cmdlet 會將應用程式新增至指定的 Azure Batch 帳戶。</span><span class="sxs-lookup"><span data-stu-id="c3ac8-106">The **New-AzBatchApplication** cmdlet adds an application to the specified Azure Batch account.</span></span>

## <span data-ttu-id="c3ac8-107">示例</span><span class="sxs-lookup"><span data-stu-id="c3ac8-107">EXAMPLES</span></span>

### <span data-ttu-id="c3ac8-108">範例1：在批次帳戶中新增空白的應用程式</span><span class="sxs-lookup"><span data-stu-id="c3ac8-108">Example 1: Add an empty application to a Batch account</span></span>
```
PS C:\>New-AzBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "Litware" -AllowUpdates $True -DisplayName "Litware Advanced Reticulator"
```

<span data-ttu-id="c3ac8-109">這個命令會在 ContosoBatch 帳戶中建立 Litware 應用程式。</span><span class="sxs-lookup"><span data-stu-id="c3ac8-109">This command creates the Litware application in the ContosoBatch account.</span></span>
<span data-ttu-id="c3ac8-110">應用程式最初不會包含任何套件。</span><span class="sxs-lookup"><span data-stu-id="c3ac8-110">The application initially contains no packages.</span></span>

## <span data-ttu-id="c3ac8-111">參數</span><span class="sxs-lookup"><span data-stu-id="c3ac8-111">PARAMETERS</span></span>

### <span data-ttu-id="c3ac8-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c3ac8-112">-AccountName</span></span>
<span data-ttu-id="c3ac8-113">指定此 Cmdlet 要新增應用程式的批次帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="c3ac8-113">Specifies the name of the Batch account to which this cmdlet adds an application.</span></span>

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

### <span data-ttu-id="c3ac8-114">-AllowUpdates</span><span class="sxs-lookup"><span data-stu-id="c3ac8-114">-AllowUpdates</span></span>
<span data-ttu-id="c3ac8-115">指定是否可使用相同的版本字串來覆寫應用程式中的套件。</span><span class="sxs-lookup"><span data-stu-id="c3ac8-115">Specifies whether packages within the application can be overwritten using the same version string.</span></span>

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

### <span data-ttu-id="c3ac8-116">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="c3ac8-116">-ApplicationId</span></span>
<span data-ttu-id="c3ac8-117">指定應用程式的識別碼。</span><span class="sxs-lookup"><span data-stu-id="c3ac8-117">Specifies the ID of the application.</span></span>

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

### <span data-ttu-id="c3ac8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3ac8-118">-DefaultProfile</span></span>
<span data-ttu-id="c3ac8-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c3ac8-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c3ac8-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="c3ac8-120">-DisplayName</span></span>
<span data-ttu-id="c3ac8-121">指定應用程式的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="c3ac8-121">Specifies the display name for the application.</span></span>

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

### <span data-ttu-id="c3ac8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3ac8-122">-ResourceGroupName</span></span>
<span data-ttu-id="c3ac8-123">指定包含批次帳戶之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c3ac8-123">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="c3ac8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3ac8-124">CommonParameters</span></span>
<span data-ttu-id="c3ac8-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c3ac8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3ac8-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c3ac8-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3ac8-127">輸入</span><span class="sxs-lookup"><span data-stu-id="c3ac8-127">INPUTS</span></span>

### <span data-ttu-id="c3ac8-128">System.object</span><span class="sxs-lookup"><span data-stu-id="c3ac8-128">System.String</span></span>

### <span data-ttu-id="c3ac8-129">"CoreLib" 1 ["System.object，System.object，版本 = 4.0.0.0，Culture = 中立，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="c3ac8-129">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="c3ac8-130">輸出</span><span class="sxs-lookup"><span data-stu-id="c3ac8-130">OUTPUTS</span></span>

### <span data-ttu-id="c3ac8-131">Microsoft.Azure.Commands.Batch。PSApplication</span><span class="sxs-lookup"><span data-stu-id="c3ac8-131">Microsoft.Azure.Commands.Batch.Models.PSApplication</span></span>

## <span data-ttu-id="c3ac8-132">筆記</span><span class="sxs-lookup"><span data-stu-id="c3ac8-132">NOTES</span></span>

## <span data-ttu-id="c3ac8-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="c3ac8-133">RELATED LINKS</span></span>

[<span data-ttu-id="c3ac8-134">AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="c3ac8-134">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="c3ac8-135">AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="c3ac8-135">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="c3ac8-136">新-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="c3ac8-136">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="c3ac8-137">移除-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="c3ac8-137">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="c3ac8-138">移除-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="c3ac8-138">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)

[<span data-ttu-id="c3ac8-139">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="c3ac8-139">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)


