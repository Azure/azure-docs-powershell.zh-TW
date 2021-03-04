---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/new-azstackedgestorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeStorageAccount.md
ms.openlocfilehash: f35e94aab5bdb59a2cc6d4c8e38cee1142c2b47a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915769"
---
# <span data-ttu-id="988a7-101">New-AzStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="988a7-101">New-AzStackEdgeStorageAccount</span></span>

## <span data-ttu-id="988a7-102">簡介</span><span class="sxs-lookup"><span data-stu-id="988a7-102">SYNOPSIS</span></span>
<span data-ttu-id="988a7-103">在裝置中建立新的 Edge 儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="988a7-103">Creates a new Edge Storage account in the device.</span></span>

## <span data-ttu-id="988a7-104">語法</span><span class="sxs-lookup"><span data-stu-id="988a7-104">SYNTAX</span></span>

```
New-AzStackEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StorageAccountCredentialName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-Cloud] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="988a7-105">描述</span><span class="sxs-lookup"><span data-stu-id="988a7-105">DESCRIPTION</span></span>
<span data-ttu-id="988a7-106">**New-AzStackEdgeStorageAccount** Cmdlet 在 Stack Edge 裝置中建立新的 Edge 儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="988a7-106">The **New-AzStackEdgeStorageAccount** cmdlet creates a new Edge Storage account in a Stack Edge device.</span></span> <span data-ttu-id="988a7-107">針對裝置，最多隻能對應到一個雲端儲存空間帳戶的一個 Edge 儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="988a7-107">For a device, one Edge Storage account can be mapped at most to only one Cloud Storage account.</span></span>

## <span data-ttu-id="988a7-108">例子</span><span class="sxs-lookup"><span data-stu-id="988a7-108">EXAMPLES</span></span>

### <span data-ttu-id="988a7-109">範例 1</span><span class="sxs-lookup"><span data-stu-id="988a7-109">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeStorageAccount -ResourceGroupName resourceGroupName -DeviceName dbEdge -Name edgestoragegacount1 -StorageAccountCredentialName cloudstorageaccount1 -Cloud
Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 0              OK     https://edgestoragegacount1.blob.dbEdge.microsoftdatabox.com/ cloudstorageaccount1     dbEdge     resourceGroupName
```

### <span data-ttu-id="988a7-110">範例 2</span><span class="sxs-lookup"><span data-stu-id="988a7-110">Example 2</span></span>
```powershell
PS C:\> New-AzStackEdgeStorageAccount -ResourceGroupName resourceGroupName -DeviceName dbEdge -Name edgestoragegacount2 -StorageAccountCredentialName cloudstorageaccount2

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.dbEdge.microsoftdatabox.com/ cloudstorageaccount2     dbEdge     resourceGroupName
```

<span data-ttu-id="988a7-111">裝置上的 2 個 EdgeStorageAccount無法共用超過 1 個雲端儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="988a7-111">2 EdgeStorageAccounts on the device cannot share more than 1 Cloud Storage Account</span></span>

## <span data-ttu-id="988a7-112">參數</span><span class="sxs-lookup"><span data-stu-id="988a7-112">PARAMETERS</span></span>

### <span data-ttu-id="988a7-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="988a7-113">-AsJob</span></span>
<span data-ttu-id="988a7-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="988a7-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="988a7-115">-雲端</span><span class="sxs-lookup"><span data-stu-id="988a7-115">-Cloud</span></span>
<span data-ttu-id="988a7-116">將使用 CloudStorageAccount進行分層</span><span class="sxs-lookup"><span data-stu-id="988a7-116">Will use a CloudStorageAccount for tiering</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="988a7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="988a7-117">-DefaultProfile</span></span>
<span data-ttu-id="988a7-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="988a7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="988a7-119">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="988a7-119">-DeviceName</span></span>
<span data-ttu-id="988a7-120">裝置名稱</span><span class="sxs-lookup"><span data-stu-id="988a7-120">Device Name</span></span>

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

### <span data-ttu-id="988a7-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="988a7-121">-Name</span></span>
<span data-ttu-id="988a7-122">資源名稱</span><span class="sxs-lookup"><span data-stu-id="988a7-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EdgeStorageAccount

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="988a7-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="988a7-123">-ResourceGroupName</span></span>
<span data-ttu-id="988a7-124">資源組名</span><span class="sxs-lookup"><span data-stu-id="988a7-124">Resource Group Name</span></span>

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

### <span data-ttu-id="988a7-125">-StorageAccountCredentialName</span><span class="sxs-lookup"><span data-stu-id="988a7-125">-StorageAccountCredentialName</span></span>
<span data-ttu-id="988a7-126">提供現有的 StorageAccountCredential 資源名稱</span><span class="sxs-lookup"><span data-stu-id="988a7-126">Provide existing StorageAccountCredential's Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="988a7-127">-確認</span><span class="sxs-lookup"><span data-stu-id="988a7-127">-Confirm</span></span>
<span data-ttu-id="988a7-128">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="988a7-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="988a7-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="988a7-129">-WhatIf</span></span>
<span data-ttu-id="988a7-130">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="988a7-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="988a7-131">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="988a7-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="988a7-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="988a7-132">CommonParameters</span></span>
<span data-ttu-id="988a7-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="988a7-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="988a7-134">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="988a7-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="988a7-135">輸入</span><span class="sxs-lookup"><span data-stu-id="988a7-135">INPUTS</span></span>

### <span data-ttu-id="988a7-136">System.String</span><span class="sxs-lookup"><span data-stu-id="988a7-136">System.String</span></span>

### <span data-ttu-id="988a7-137">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="988a7-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="988a7-138">輸出</span><span class="sxs-lookup"><span data-stu-id="988a7-138">OUTPUTS</span></span>

### <span data-ttu-id="988a7-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.models.PSStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="988a7-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount</span></span>

## <span data-ttu-id="988a7-140">筆記</span><span class="sxs-lookup"><span data-stu-id="988a7-140">NOTES</span></span>

## <span data-ttu-id="988a7-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="988a7-141">RELATED LINKS</span></span>
