---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: CF8B8E94-3C6C-4D68-B55B-956393890946
online version: https://docs.microsoft.com/powershell/module/az.batch/get-azbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchApplication.md
ms.openlocfilehash: b32c0d7db6a55a560733380c66e971c614fabc71
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906974"
---
# <span data-ttu-id="af362-101">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="af362-101">Get-AzBatchApplication</span></span>

## <span data-ttu-id="af362-102">簡介</span><span class="sxs-lookup"><span data-stu-id="af362-102">SYNOPSIS</span></span>
<span data-ttu-id="af362-103">獲得指定應用程式的資訊。</span><span class="sxs-lookup"><span data-stu-id="af362-103">Gets information about the specified application.</span></span>

## <span data-ttu-id="af362-104">語法</span><span class="sxs-lookup"><span data-stu-id="af362-104">SYNTAX</span></span>

```
Get-AzBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [[-ApplicationName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="af362-105">描述</span><span class="sxs-lookup"><span data-stu-id="af362-105">DESCRIPTION</span></span>
<span data-ttu-id="af362-106">**Get-AzBatchApplication** Cmdlet 會取得 Azure Batch 帳戶中應用程式的資訊。</span><span class="sxs-lookup"><span data-stu-id="af362-106">The **Get-AzBatchApplication** cmdlet gets information about an application in an Azure Batch account.</span></span>

## <span data-ttu-id="af362-107">例子</span><span class="sxs-lookup"><span data-stu-id="af362-107">EXAMPLES</span></span>

### <span data-ttu-id="af362-108">範例 1：在批次處理帳戶中顯示應用程式</span><span class="sxs-lookup"><span data-stu-id="af362-108">Example 1: Display the applications in a Batch account</span></span>
```
PS C:\>Get-AzBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup"
ApplicationName AllowUpdates DisplayName

------------- ------------ ----------------------------

litware       False        Litware Advanced Reticulator
```

<span data-ttu-id="af362-109">此命令會顯示 ContosoBatch 帳戶中的所有應用程式。</span><span class="sxs-lookup"><span data-stu-id="af362-109">This command displays all applications in the ContosoBatch account.</span></span>

## <span data-ttu-id="af362-110">參數</span><span class="sxs-lookup"><span data-stu-id="af362-110">PARAMETERS</span></span>

### <span data-ttu-id="af362-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="af362-111">-AccountName</span></span>
<span data-ttu-id="af362-112">指定包含應用程式的 Batch 帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="af362-112">Specifies the name of the Batch account that contains the application.</span></span>

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

### <span data-ttu-id="af362-113">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="af362-113">-ApplicationName</span></span>
<span data-ttu-id="af362-114">指定應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="af362-114">Specifies the name of the application.</span></span>

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

### <span data-ttu-id="af362-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af362-115">-DefaultProfile</span></span>
<span data-ttu-id="af362-116">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="af362-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="af362-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af362-117">-ResourceGroupName</span></span>
<span data-ttu-id="af362-118">指定包含批次帳戶的資源組名。</span><span class="sxs-lookup"><span data-stu-id="af362-118">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="af362-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af362-119">CommonParameters</span></span>
<span data-ttu-id="af362-120">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="af362-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af362-121">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="af362-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af362-122">輸入</span><span class="sxs-lookup"><span data-stu-id="af362-122">INPUTS</span></span>

### <span data-ttu-id="af362-123">System.String</span><span class="sxs-lookup"><span data-stu-id="af362-123">System.String</span></span>

## <span data-ttu-id="af362-124">輸出</span><span class="sxs-lookup"><span data-stu-id="af362-124">OUTPUTS</span></span>

### <span data-ttu-id="af362-125">Microsoft.Azure.Commands.Batch。Models.PSApplication</span><span class="sxs-lookup"><span data-stu-id="af362-125">Microsoft.Azure.Commands.Batch.Models.PSApplication</span></span>

## <span data-ttu-id="af362-126">筆記</span><span class="sxs-lookup"><span data-stu-id="af362-126">NOTES</span></span>

## <span data-ttu-id="af362-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="af362-127">RELATED LINKS</span></span>

[<span data-ttu-id="af362-128">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="af362-128">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="af362-129">New-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="af362-129">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="af362-130">New-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="af362-130">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="af362-131">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="af362-131">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="af362-132">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="af362-132">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)

[<span data-ttu-id="af362-133">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="af362-133">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)


