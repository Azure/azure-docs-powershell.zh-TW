---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 2CED21D6-4BEF-423B-A04A-5B812CEB975D
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchApplication.md
ms.openlocfilehash: 65840269419ee0cdfe322c9c6906e8ac4b368d1b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93970641"
---
# <span data-ttu-id="37b31-101">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="37b31-101">Remove-AzBatchApplication</span></span>

## <span data-ttu-id="37b31-102">摘要</span><span class="sxs-lookup"><span data-stu-id="37b31-102">SYNOPSIS</span></span>
<span data-ttu-id="37b31-103">從批次帳戶刪除應用程式。</span><span class="sxs-lookup"><span data-stu-id="37b31-103">Deletes an application from a Batch account.</span></span>

## <span data-ttu-id="37b31-104">句法</span><span class="sxs-lookup"><span data-stu-id="37b31-104">SYNTAX</span></span>

```
Remove-AzBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="37b31-105">說明</span><span class="sxs-lookup"><span data-stu-id="37b31-105">DESCRIPTION</span></span>
<span data-ttu-id="37b31-106">**AzBatchApplication** Cmdlet 會從 Azure Batch 帳戶刪除應用程式。</span><span class="sxs-lookup"><span data-stu-id="37b31-106">The **Remove-AzBatchApplication** cmdlet deletes an application from an Azure Batch account.</span></span>

## <span data-ttu-id="37b31-107">示例</span><span class="sxs-lookup"><span data-stu-id="37b31-107">EXAMPLES</span></span>

### <span data-ttu-id="37b31-108">範例1：從批次帳戶刪除應用程式</span><span class="sxs-lookup"><span data-stu-id="37b31-108">Example 1: Delete an application from a Batch account</span></span>
```
PS C:\>Remove-AzBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationName "Litware"
```

<span data-ttu-id="37b31-109">這個命令會從 ContosoBatch 帳戶刪除 Litware 應用程式。</span><span class="sxs-lookup"><span data-stu-id="37b31-109">This command deletes the Litware application from the ContosoBatch account.</span></span>
<span data-ttu-id="37b31-110">如果應用程式包含任何套件，命令就會失敗。</span><span class="sxs-lookup"><span data-stu-id="37b31-110">The command fails if the application contains any packages.</span></span>

## <span data-ttu-id="37b31-111">參數</span><span class="sxs-lookup"><span data-stu-id="37b31-111">PARAMETERS</span></span>

### <span data-ttu-id="37b31-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="37b31-112">-AccountName</span></span>
<span data-ttu-id="37b31-113">指定此 Cmdlet 從中移除應用程式的批次帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="37b31-113">Specifies the name of the Batch account from which this cmdlet removes an application.</span></span>

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

### <span data-ttu-id="37b31-114">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="37b31-114">-ApplicationName</span></span>
<span data-ttu-id="37b31-115">指定應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="37b31-115">Specifies the name of the application.</span></span>

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

### <span data-ttu-id="37b31-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37b31-116">-DefaultProfile</span></span>
<span data-ttu-id="37b31-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="37b31-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="37b31-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37b31-118">-ResourceGroupName</span></span>
<span data-ttu-id="37b31-119">指定包含批次帳戶之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="37b31-119">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="37b31-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37b31-120">CommonParameters</span></span>
<span data-ttu-id="37b31-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="37b31-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37b31-122">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="37b31-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37b31-123">輸入</span><span class="sxs-lookup"><span data-stu-id="37b31-123">INPUTS</span></span>

### <span data-ttu-id="37b31-124">System.object</span><span class="sxs-lookup"><span data-stu-id="37b31-124">System.String</span></span>

## <span data-ttu-id="37b31-125">輸出</span><span class="sxs-lookup"><span data-stu-id="37b31-125">OUTPUTS</span></span>

### <span data-ttu-id="37b31-126">System.void</span><span class="sxs-lookup"><span data-stu-id="37b31-126">System.Void</span></span>

## <span data-ttu-id="37b31-127">筆記</span><span class="sxs-lookup"><span data-stu-id="37b31-127">NOTES</span></span>

## <span data-ttu-id="37b31-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="37b31-128">RELATED LINKS</span></span>

[<span data-ttu-id="37b31-129">AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="37b31-129">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="37b31-130">AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="37b31-130">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="37b31-131">新-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="37b31-131">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="37b31-132">新-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="37b31-132">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="37b31-133">移除-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="37b31-133">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)

[<span data-ttu-id="37b31-134">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="37b31-134">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)


