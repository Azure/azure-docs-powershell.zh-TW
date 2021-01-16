---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: CF8B8E94-3C6C-4D68-B55B-956393890946
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchApplication.md
ms.openlocfilehash: efdcab51a8dfa6d886a317fa1707b65861cf2563
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98278977"
---
# <span data-ttu-id="43b2f-101">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="43b2f-101">Get-AzBatchApplication</span></span>

## <span data-ttu-id="43b2f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="43b2f-102">SYNOPSIS</span></span>
<span data-ttu-id="43b2f-103">取得特定應用程式的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="43b2f-103">Gets information about the specified application.</span></span>

## <span data-ttu-id="43b2f-104">句法</span><span class="sxs-lookup"><span data-stu-id="43b2f-104">SYNTAX</span></span>

```
Get-AzBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [[-ApplicationName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="43b2f-105">說明</span><span class="sxs-lookup"><span data-stu-id="43b2f-105">DESCRIPTION</span></span>
<span data-ttu-id="43b2f-106">**AzBatchApplication** Cmdlet 會取得 Azure Batch 帳戶中應用程式的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="43b2f-106">The **Get-AzBatchApplication** cmdlet gets information about an application in an Azure Batch account.</span></span>

## <span data-ttu-id="43b2f-107">示例</span><span class="sxs-lookup"><span data-stu-id="43b2f-107">EXAMPLES</span></span>

### <span data-ttu-id="43b2f-108">範例1：以批次帳戶顯示應用程式</span><span class="sxs-lookup"><span data-stu-id="43b2f-108">Example 1: Display the applications in a Batch account</span></span>
```
PS C:\>Get-AzBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup"
ApplicationName AllowUpdates DisplayName

------------- ------------ ----------------------------

litware       False        Litware Advanced Reticulator
```

<span data-ttu-id="43b2f-109">這個命令會顯示 ContosoBatch 帳戶中的所有應用程式。</span><span class="sxs-lookup"><span data-stu-id="43b2f-109">This command displays all applications in the ContosoBatch account.</span></span>

## <span data-ttu-id="43b2f-110">參數</span><span class="sxs-lookup"><span data-stu-id="43b2f-110">PARAMETERS</span></span>

### <span data-ttu-id="43b2f-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="43b2f-111">-AccountName</span></span>
<span data-ttu-id="43b2f-112">指定包含應用程式的批次帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="43b2f-112">Specifies the name of the Batch account that contains the application.</span></span>

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

### <span data-ttu-id="43b2f-113">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="43b2f-113">-ApplicationName</span></span>
<span data-ttu-id="43b2f-114">指定應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="43b2f-114">Specifies the name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationId

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43b2f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43b2f-115">-DefaultProfile</span></span>
<span data-ttu-id="43b2f-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="43b2f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="43b2f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43b2f-117">-ResourceGroupName</span></span>
<span data-ttu-id="43b2f-118">指定包含批次帳戶之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="43b2f-118">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="43b2f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43b2f-119">CommonParameters</span></span>
<span data-ttu-id="43b2f-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="43b2f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43b2f-121">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="43b2f-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43b2f-122">輸入</span><span class="sxs-lookup"><span data-stu-id="43b2f-122">INPUTS</span></span>

### <span data-ttu-id="43b2f-123">System.object</span><span class="sxs-lookup"><span data-stu-id="43b2f-123">System.String</span></span>

## <span data-ttu-id="43b2f-124">輸出</span><span class="sxs-lookup"><span data-stu-id="43b2f-124">OUTPUTS</span></span>

### <span data-ttu-id="43b2f-125">Microsoft.Azure.Commands.Batch。PSApplication</span><span class="sxs-lookup"><span data-stu-id="43b2f-125">Microsoft.Azure.Commands.Batch.Models.PSApplication</span></span>

## <span data-ttu-id="43b2f-126">筆記</span><span class="sxs-lookup"><span data-stu-id="43b2f-126">NOTES</span></span>

## <span data-ttu-id="43b2f-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="43b2f-127">RELATED LINKS</span></span>

[<span data-ttu-id="43b2f-128">AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="43b2f-128">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="43b2f-129">新-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="43b2f-129">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="43b2f-130">新-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="43b2f-130">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="43b2f-131">移除-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="43b2f-131">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="43b2f-132">移除-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="43b2f-132">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)

[<span data-ttu-id="43b2f-133">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="43b2f-133">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)


