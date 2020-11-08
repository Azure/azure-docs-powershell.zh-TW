---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgestorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeStorageAccount.md
ms.openlocfilehash: 815b8a7feb22e754302c455c7666f8408c348c92
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94141018"
---
# <span data-ttu-id="60e84-101">New-AzStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="60e84-101">New-AzStackEdgeStorageAccount</span></span>

## <span data-ttu-id="60e84-102">摘要</span><span class="sxs-lookup"><span data-stu-id="60e84-102">SYNOPSIS</span></span>
<span data-ttu-id="60e84-103">在裝置中建立新的邊緣儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="60e84-103">Creates a new Edge Storage account in the device.</span></span>

## <span data-ttu-id="60e84-104">句法</span><span class="sxs-lookup"><span data-stu-id="60e84-104">SYNTAX</span></span>

```
New-AzStackEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StorageAccountCredentialName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-Cloud] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60e84-105">說明</span><span class="sxs-lookup"><span data-stu-id="60e84-105">DESCRIPTION</span></span>
<span data-ttu-id="60e84-106">**新的-AzStackEdgeStorageAccount** Cmdlet 會在堆疊 Edge 裝置中建立新的 Edge 儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="60e84-106">The **New-AzStackEdgeStorageAccount** cmdlet creates a new Edge Storage account in a Stack Edge device.</span></span> <span data-ttu-id="60e84-107">針對裝置，一個 Edge 儲存空間帳戶最多隻能對應一個雲端儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="60e84-107">For a device, one Edge Storage account can be mapped at most to only one Cloud Storage account.</span></span>

## <span data-ttu-id="60e84-108">示例</span><span class="sxs-lookup"><span data-stu-id="60e84-108">EXAMPLES</span></span>

### <span data-ttu-id="60e84-109">範例1</span><span class="sxs-lookup"><span data-stu-id="60e84-109">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeStorageAccount -ResourceGroupName resourceGroupName -DeviceName dbEdge -Name edgestoragegacount1 -StorageAccountCredentialName cloudstorageaccount1 -Cloud
Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 0              OK     https://edgestoragegacount1.blob.dbEdge.microsoftdatabox.com/ cloudstorageaccount1     dbEdge     resourceGroupName
```

### <span data-ttu-id="60e84-110">範例2</span><span class="sxs-lookup"><span data-stu-id="60e84-110">Example 2</span></span>
```powershell
PS C:\> New-AzStackEdgeStorageAccount -ResourceGroupName resourceGroupName -DeviceName dbEdge -Name edgestoragegacount2 -StorageAccountCredentialName cloudstorageaccount2

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.dbEdge.microsoftdatabox.com/ cloudstorageaccount2     dbEdge     resourceGroupName
```

<span data-ttu-id="60e84-111">裝置上的2個 EdgeStorageAccounts 無法共用1個以上的雲端儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="60e84-111">2 EdgeStorageAccounts on the device cannot share more than 1 Cloud Storage Account</span></span>

## <span data-ttu-id="60e84-112">參數</span><span class="sxs-lookup"><span data-stu-id="60e84-112">PARAMETERS</span></span>

### <span data-ttu-id="60e84-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="60e84-113">-AsJob</span></span>
<span data-ttu-id="60e84-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="60e84-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="60e84-115">-雲端</span><span class="sxs-lookup"><span data-stu-id="60e84-115">-Cloud</span></span>
<span data-ttu-id="60e84-116">將使用 CloudStorageAccount 進行堆疊</span><span class="sxs-lookup"><span data-stu-id="60e84-116">Will use a CloudStorageAccount for tiering</span></span>

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

### <span data-ttu-id="60e84-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60e84-117">-DefaultProfile</span></span>
<span data-ttu-id="60e84-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="60e84-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60e84-119">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="60e84-119">-DeviceName</span></span>
<span data-ttu-id="60e84-120">裝置名稱</span><span class="sxs-lookup"><span data-stu-id="60e84-120">Device Name</span></span>

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

### <span data-ttu-id="60e84-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="60e84-121">-Name</span></span>
<span data-ttu-id="60e84-122">資源名稱</span><span class="sxs-lookup"><span data-stu-id="60e84-122">Resource Name</span></span>

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

### <span data-ttu-id="60e84-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60e84-123">-ResourceGroupName</span></span>
<span data-ttu-id="60e84-124">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="60e84-124">Resource Group Name</span></span>

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

### <span data-ttu-id="60e84-125">-StorageAccountCredentialName</span><span class="sxs-lookup"><span data-stu-id="60e84-125">-StorageAccountCredentialName</span></span>
<span data-ttu-id="60e84-126">提供現有 StorageAccountCredential 的資源名稱</span><span class="sxs-lookup"><span data-stu-id="60e84-126">Provide existing StorageAccountCredential's Resource Name</span></span>

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

### <span data-ttu-id="60e84-127">-確認</span><span class="sxs-lookup"><span data-stu-id="60e84-127">-Confirm</span></span>
<span data-ttu-id="60e84-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="60e84-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60e84-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60e84-129">-WhatIf</span></span>
<span data-ttu-id="60e84-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="60e84-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="60e84-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="60e84-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60e84-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60e84-132">CommonParameters</span></span>
<span data-ttu-id="60e84-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="60e84-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60e84-134">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="60e84-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60e84-135">輸入</span><span class="sxs-lookup"><span data-stu-id="60e84-135">INPUTS</span></span>

### <span data-ttu-id="60e84-136">System.object</span><span class="sxs-lookup"><span data-stu-id="60e84-136">System.String</span></span>

### <span data-ttu-id="60e84-137">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="60e84-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="60e84-138">輸出</span><span class="sxs-lookup"><span data-stu-id="60e84-138">OUTPUTS</span></span>

### <span data-ttu-id="60e84-139">PSStackEdgeStorageAccount （StackEdge）的</span><span class="sxs-lookup"><span data-stu-id="60e84-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount</span></span>

## <span data-ttu-id="60e84-140">筆記</span><span class="sxs-lookup"><span data-stu-id="60e84-140">NOTES</span></span>

## <span data-ttu-id="60e84-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="60e84-141">RELATED LINKS</span></span>