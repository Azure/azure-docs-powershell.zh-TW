---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: DCA1FD7A-54AF-48B1-A245-BFA9C43ACA9B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/set-azurermbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureRmBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureRmBatchApplication.md
ms.openlocfilehash: 8ede896e6a49cee5305e7f9fd42f6dab130e7986
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450283"
---
# <span data-ttu-id="a2419-101">Set-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="a2419-101">Set-AzureRmBatchApplication</span></span>

## <span data-ttu-id="a2419-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a2419-102">SYNOPSIS</span></span>
<span data-ttu-id="a2419-103">更新指定應用程式的設定。</span><span class="sxs-lookup"><span data-stu-id="a2419-103">Updates settings for the specified application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a2419-104">句法</span><span class="sxs-lookup"><span data-stu-id="a2419-104">SYNTAX</span></span>

```
Set-AzureRmBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationId] <String>
 [[-DisplayName] <String>] [[-DefaultVersion] <String>] [[-AllowUpdates] <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a2419-105">說明</span><span class="sxs-lookup"><span data-stu-id="a2419-105">DESCRIPTION</span></span>
<span data-ttu-id="a2419-106">**AzureRmBatchApplication** Cmdlet 會修改指定 Azure 批次應用程式的設定。</span><span class="sxs-lookup"><span data-stu-id="a2419-106">The **Set-AzureRmBatchApplication** cmdlet modifies settings for the specified Azure Batch application.</span></span>

## <span data-ttu-id="a2419-107">示例</span><span class="sxs-lookup"><span data-stu-id="a2419-107">EXAMPLES</span></span>

### <span data-ttu-id="a2419-108">範例1：更新批次帳戶中的應用程式</span><span class="sxs-lookup"><span data-stu-id="a2419-108">Example 1: Update an application in a Batch account</span></span>
```
PS C:\>Set-AzureRmBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "Litware" -AllowUpdates $False
```

<span data-ttu-id="a2419-109">這個命令會變更 ContosoBatch 帳戶中的 Llitware 應用程式是否允許更新。</span><span class="sxs-lookup"><span data-stu-id="a2419-109">This command changes whether the Llitware application in the ContosoBatch account allows updates.</span></span>
<span data-ttu-id="a2419-110">此命令不會變更應用程式的預設版本或顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="a2419-110">The command does not change the default version or display name of the application.</span></span>

## <span data-ttu-id="a2419-111">參數</span><span class="sxs-lookup"><span data-stu-id="a2419-111">PARAMETERS</span></span>

### <span data-ttu-id="a2419-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a2419-112">-AccountName</span></span>
<span data-ttu-id="a2419-113">指定此 Cmdlet 修改應用程式的批次帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="a2419-113">Specifies the name of the Batch account for which this cmdlet modifies an application.</span></span>

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

### <span data-ttu-id="a2419-114">-AllowUpdates</span><span class="sxs-lookup"><span data-stu-id="a2419-114">-AllowUpdates</span></span>
<span data-ttu-id="a2419-115">指定是否可使用相同的版本字串來覆寫應用程式中的套件。</span><span class="sxs-lookup"><span data-stu-id="a2419-115">Specifies whether packages within the application can be overwritten using the same version string.</span></span>

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

### <span data-ttu-id="a2419-116">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="a2419-116">-ApplicationId</span></span>
<span data-ttu-id="a2419-117">指定應用程式的識別碼。</span><span class="sxs-lookup"><span data-stu-id="a2419-117">Specifies the ID of the application.</span></span>

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

### <span data-ttu-id="a2419-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2419-118">-DefaultProfile</span></span>
<span data-ttu-id="a2419-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a2419-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2419-120">-DefaultVersion</span><span class="sxs-lookup"><span data-stu-id="a2419-120">-DefaultVersion</span></span>
<span data-ttu-id="a2419-121">指定用戶端要求應用程式但未指定版本時要使用的套件。</span><span class="sxs-lookup"><span data-stu-id="a2419-121">Specifies which package to use if a client requests the application but does not specify a version.</span></span>

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

### <span data-ttu-id="a2419-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="a2419-122">-DisplayName</span></span>
<span data-ttu-id="a2419-123">指定應用程式的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="a2419-123">Specifies the display name for the application.</span></span>

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

### <span data-ttu-id="a2419-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2419-124">-ResourceGroupName</span></span>
<span data-ttu-id="a2419-125">指定包含批次帳戶之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a2419-125">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="a2419-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2419-126">CommonParameters</span></span>
<span data-ttu-id="a2419-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a2419-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2419-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a2419-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2419-129">輸入</span><span class="sxs-lookup"><span data-stu-id="a2419-129">INPUTS</span></span>

### <span data-ttu-id="a2419-130">System.object</span><span class="sxs-lookup"><span data-stu-id="a2419-130">System.String</span></span>

### <span data-ttu-id="a2419-131">系統為 Nullable "1 [[System.object，mscorlib，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="a2419-131">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="a2419-132">輸出</span><span class="sxs-lookup"><span data-stu-id="a2419-132">OUTPUTS</span></span>

### <span data-ttu-id="a2419-133">System.void</span><span class="sxs-lookup"><span data-stu-id="a2419-133">System.Void</span></span>

## <span data-ttu-id="a2419-134">筆記</span><span class="sxs-lookup"><span data-stu-id="a2419-134">NOTES</span></span>

## <span data-ttu-id="a2419-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="a2419-135">RELATED LINKS</span></span>

[<span data-ttu-id="a2419-136">AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="a2419-136">Get-AzureRmBatchApplication</span></span>](./Get-AzureRmBatchApplication.md)

[<span data-ttu-id="a2419-137">AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="a2419-137">Get-AzureRmBatchApplicationPackage</span></span>](./Get-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="a2419-138">新-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="a2419-138">New-AzureRmBatchApplication</span></span>](./New-AzureRmBatchApplication.md)

[<span data-ttu-id="a2419-139">新-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="a2419-139">New-AzureRmBatchApplicationPackage</span></span>](./New-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="a2419-140">移除-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="a2419-140">Remove-AzureRmBatchApplication</span></span>](./Remove-AzureRmBatchApplication.md)

[<span data-ttu-id="a2419-141">移除-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="a2419-141">Remove-AzureRmBatchApplicationPackage</span></span>](./Remove-AzureRmBatchApplicationPackage.md)


