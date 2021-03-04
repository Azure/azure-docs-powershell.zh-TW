---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 2CED21D6-4BEF-423B-A04A-5B812CEB975D
online version: https://docs.microsoft.com/powershell/module/az.batch/remove-azbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchApplication.md
ms.openlocfilehash: ebe28df5c69ce966a9d05d2e34cd9e66693d7f4b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912465"
---
# <span data-ttu-id="6a77c-101">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="6a77c-101">Remove-AzBatchApplication</span></span>

## <span data-ttu-id="6a77c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="6a77c-102">SYNOPSIS</span></span>
<span data-ttu-id="6a77c-103">從批次帳戶刪除應用程式。</span><span class="sxs-lookup"><span data-stu-id="6a77c-103">Deletes an application from a Batch account.</span></span>

## <span data-ttu-id="6a77c-104">語法</span><span class="sxs-lookup"><span data-stu-id="6a77c-104">SYNTAX</span></span>

```
Remove-AzBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6a77c-105">描述</span><span class="sxs-lookup"><span data-stu-id="6a77c-105">DESCRIPTION</span></span>
<span data-ttu-id="6a77c-106">**Remove-AzBatchApplication** Cmdlet 會從 Azure Batch 帳戶刪除應用程式。</span><span class="sxs-lookup"><span data-stu-id="6a77c-106">The **Remove-AzBatchApplication** cmdlet deletes an application from an Azure Batch account.</span></span>

## <span data-ttu-id="6a77c-107">例子</span><span class="sxs-lookup"><span data-stu-id="6a77c-107">EXAMPLES</span></span>

### <span data-ttu-id="6a77c-108">範例 1：從 Batch 帳戶刪除應用程式</span><span class="sxs-lookup"><span data-stu-id="6a77c-108">Example 1: Delete an application from a Batch account</span></span>
```
PS C:\>Remove-AzBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationName "Litware"
```

<span data-ttu-id="6a77c-109">此命令會從 ContosoBatch 帳戶刪除 Litware 應用程式。</span><span class="sxs-lookup"><span data-stu-id="6a77c-109">This command deletes the Litware application from the ContosoBatch account.</span></span>
<span data-ttu-id="6a77c-110">如果應用程式包含任何套件，該命令會失敗。</span><span class="sxs-lookup"><span data-stu-id="6a77c-110">The command fails if the application contains any packages.</span></span>

## <span data-ttu-id="6a77c-111">參數</span><span class="sxs-lookup"><span data-stu-id="6a77c-111">PARAMETERS</span></span>

### <span data-ttu-id="6a77c-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="6a77c-112">-AccountName</span></span>
<span data-ttu-id="6a77c-113">指定此 Cmdlet 移除應用程式的 Batch 帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="6a77c-113">Specifies the name of the Batch account from which this cmdlet removes an application.</span></span>

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

### <span data-ttu-id="6a77c-114">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="6a77c-114">-ApplicationName</span></span>
<span data-ttu-id="6a77c-115">指定應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="6a77c-115">Specifies the name of the application.</span></span>

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

### <span data-ttu-id="6a77c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a77c-116">-DefaultProfile</span></span>
<span data-ttu-id="6a77c-117">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="6a77c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6a77c-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a77c-118">-ResourceGroupName</span></span>
<span data-ttu-id="6a77c-119">指定包含批次帳戶的資源組名。</span><span class="sxs-lookup"><span data-stu-id="6a77c-119">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="6a77c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a77c-120">CommonParameters</span></span>
<span data-ttu-id="6a77c-121">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="6a77c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a77c-122">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6a77c-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a77c-123">輸入</span><span class="sxs-lookup"><span data-stu-id="6a77c-123">INPUTS</span></span>

### <span data-ttu-id="6a77c-124">System.String</span><span class="sxs-lookup"><span data-stu-id="6a77c-124">System.String</span></span>

## <span data-ttu-id="6a77c-125">輸出</span><span class="sxs-lookup"><span data-stu-id="6a77c-125">OUTPUTS</span></span>

### <span data-ttu-id="6a77c-126">System.Void</span><span class="sxs-lookup"><span data-stu-id="6a77c-126">System.Void</span></span>

## <span data-ttu-id="6a77c-127">筆記</span><span class="sxs-lookup"><span data-stu-id="6a77c-127">NOTES</span></span>

## <span data-ttu-id="6a77c-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="6a77c-128">RELATED LINKS</span></span>

[<span data-ttu-id="6a77c-129">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="6a77c-129">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="6a77c-130">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="6a77c-130">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="6a77c-131">New-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="6a77c-131">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="6a77c-132">New-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="6a77c-132">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="6a77c-133">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="6a77c-133">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)

[<span data-ttu-id="6a77c-134">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="6a77c-134">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)


