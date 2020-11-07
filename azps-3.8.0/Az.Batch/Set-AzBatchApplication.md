---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: DCA1FD7A-54AF-48B1-A245-BFA9C43ACA9B
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchApplication.md
ms.openlocfilehash: 6d6c72702d03b3b2174c21c786fb373374cea739
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958369"
---
# <span data-ttu-id="fecf1-101">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="fecf1-101">Set-AzBatchApplication</span></span>

## <span data-ttu-id="fecf1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fecf1-102">SYNOPSIS</span></span>
<span data-ttu-id="fecf1-103">更新指定應用程式的設定。</span><span class="sxs-lookup"><span data-stu-id="fecf1-103">Updates settings for the specified application.</span></span>

## <span data-ttu-id="fecf1-104">句法</span><span class="sxs-lookup"><span data-stu-id="fecf1-104">SYNTAX</span></span>

```
Set-AzBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationName] <String>
 [[-DisplayName] <String>] [[-DefaultVersion] <String>] [[-AllowUpdates] <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fecf1-105">說明</span><span class="sxs-lookup"><span data-stu-id="fecf1-105">DESCRIPTION</span></span>
<span data-ttu-id="fecf1-106">**AzBatchApplication** Cmdlet 會修改指定 Azure 批次應用程式的設定。</span><span class="sxs-lookup"><span data-stu-id="fecf1-106">The **Set-AzBatchApplication** cmdlet modifies settings for the specified Azure Batch application.</span></span>

## <span data-ttu-id="fecf1-107">示例</span><span class="sxs-lookup"><span data-stu-id="fecf1-107">EXAMPLES</span></span>

### <span data-ttu-id="fecf1-108">範例1：更新批次帳戶中的應用程式</span><span class="sxs-lookup"><span data-stu-id="fecf1-108">Example 1: Update an application in a Batch account</span></span>
```
PS C:\>Set-AzBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationName "Litware" -AllowUpdates $False
```

<span data-ttu-id="fecf1-109">這個命令會變更 ContosoBatch 帳戶中的 Litware 應用程式是否允許更新。</span><span class="sxs-lookup"><span data-stu-id="fecf1-109">This command changes whether the Litware application in the ContosoBatch account allows updates.</span></span>
<span data-ttu-id="fecf1-110">此命令不會變更應用程式的預設版本或顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="fecf1-110">The command does not change the default version or display name of the application.</span></span>

## <span data-ttu-id="fecf1-111">參數</span><span class="sxs-lookup"><span data-stu-id="fecf1-111">PARAMETERS</span></span>

### <span data-ttu-id="fecf1-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="fecf1-112">-AccountName</span></span>
<span data-ttu-id="fecf1-113">指定此 Cmdlet 修改應用程式的批次帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="fecf1-113">Specifies the name of the Batch account for which this cmdlet modifies an application.</span></span>

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

### <span data-ttu-id="fecf1-114">-AllowUpdates</span><span class="sxs-lookup"><span data-stu-id="fecf1-114">-AllowUpdates</span></span>
<span data-ttu-id="fecf1-115">指定是否可使用相同的版本字串來覆寫應用程式中的套件。</span><span class="sxs-lookup"><span data-stu-id="fecf1-115">Specifies whether packages within the application can be overwritten using the same version string.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fecf1-116">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="fecf1-116">-ApplicationName</span></span>
<span data-ttu-id="fecf1-117">指定應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="fecf1-117">Specifies the name of the application.</span></span>

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

### <span data-ttu-id="fecf1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fecf1-118">-DefaultProfile</span></span>
<span data-ttu-id="fecf1-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fecf1-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fecf1-120">-DefaultVersion</span><span class="sxs-lookup"><span data-stu-id="fecf1-120">-DefaultVersion</span></span>
<span data-ttu-id="fecf1-121">指定用戶端要求應用程式但未指定版本時要使用的套件。</span><span class="sxs-lookup"><span data-stu-id="fecf1-121">Specifies which package to use if a client requests the application but does not specify a version.</span></span>

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

### <span data-ttu-id="fecf1-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="fecf1-122">-DisplayName</span></span>
<span data-ttu-id="fecf1-123">指定應用程式的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="fecf1-123">Specifies the display name for the application.</span></span>

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

### <span data-ttu-id="fecf1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fecf1-124">-ResourceGroupName</span></span>
<span data-ttu-id="fecf1-125">指定包含批次帳戶之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="fecf1-125">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="fecf1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fecf1-126">CommonParameters</span></span>
<span data-ttu-id="fecf1-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fecf1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fecf1-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="fecf1-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fecf1-129">輸入</span><span class="sxs-lookup"><span data-stu-id="fecf1-129">INPUTS</span></span>

### <span data-ttu-id="fecf1-130">System.object</span><span class="sxs-lookup"><span data-stu-id="fecf1-130">System.String</span></span>

### <span data-ttu-id="fecf1-131">系統為 Nullable "1 [[System.object，mscorlib，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="fecf1-131">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="fecf1-132">輸出</span><span class="sxs-lookup"><span data-stu-id="fecf1-132">OUTPUTS</span></span>

### <span data-ttu-id="fecf1-133">System.void</span><span class="sxs-lookup"><span data-stu-id="fecf1-133">System.Void</span></span>

## <span data-ttu-id="fecf1-134">筆記</span><span class="sxs-lookup"><span data-stu-id="fecf1-134">NOTES</span></span>

## <span data-ttu-id="fecf1-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="fecf1-135">RELATED LINKS</span></span>

[<span data-ttu-id="fecf1-136">AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="fecf1-136">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="fecf1-137">AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="fecf1-137">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="fecf1-138">新-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="fecf1-138">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="fecf1-139">新-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="fecf1-139">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="fecf1-140">移除-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="fecf1-140">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="fecf1-141">移除-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="fecf1-141">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)


