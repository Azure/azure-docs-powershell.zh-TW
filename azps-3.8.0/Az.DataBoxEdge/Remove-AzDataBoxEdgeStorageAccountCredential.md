---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeStorageAccountCredential.md
ms.openlocfilehash: 00cfc136465cc250d068344158d66f98dc6e0704
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93966014"
---
# <span data-ttu-id="70441-101">Remove-AzDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="70441-101">Remove-AzDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="70441-102">摘要</span><span class="sxs-lookup"><span data-stu-id="70441-102">SYNOPSIS</span></span>
<span data-ttu-id="70441-103">移除裝置的儲存帳號憑證。</span><span class="sxs-lookup"><span data-stu-id="70441-103">Removes a storage account credential for a device.</span></span>

## <span data-ttu-id="70441-104">句法</span><span class="sxs-lookup"><span data-stu-id="70441-104">SYNTAX</span></span>

### <span data-ttu-id="70441-105">DeleteByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="70441-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String>
 [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="70441-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="70441-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeStorageAccountCredential [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70441-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="70441-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeStorageAccountCredential [-InputObject] <PSDataBoxEdgeStorageAccountCredential> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70441-108">說明</span><span class="sxs-lookup"><span data-stu-id="70441-108">DESCRIPTION</span></span>
<span data-ttu-id="70441-109">**AzDataBoxEdgeStorageAccountCredential** Cmdlet 會移除資料盒 Edge 裝置的儲存帳號憑證。</span><span class="sxs-lookup"><span data-stu-id="70441-109">The **Remove-AzDataBoxEdgeStorageAccountCredential** cmdlet removes the storage account credential for a Data Box Edge device.</span></span>

## <span data-ttu-id="70441-110">示例</span><span class="sxs-lookup"><span data-stu-id="70441-110">EXAMPLES</span></span>

### <span data-ttu-id="70441-111">範例1</span><span class="sxs-lookup"><span data-stu-id="70441-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeStorageAccountCredential ResourceGroupName resourceGroupName -DeviceName deviceName -Name storageAccountCredentialName
```

## <span data-ttu-id="70441-112">參數</span><span class="sxs-lookup"><span data-stu-id="70441-112">PARAMETERS</span></span>

### <span data-ttu-id="70441-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="70441-113">-AsJob</span></span>
<span data-ttu-id="70441-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="70441-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="70441-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70441-115">-DefaultProfile</span></span>
<span data-ttu-id="70441-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="70441-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="70441-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="70441-117">-DeviceName</span></span>
<span data-ttu-id="70441-118">裝置名稱</span><span class="sxs-lookup"><span data-stu-id="70441-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70441-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="70441-119">-InputObject</span></span>
<span data-ttu-id="70441-120">輸入物件</span><span class="sxs-lookup"><span data-stu-id="70441-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="70441-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="70441-121">-Name</span></span>
<span data-ttu-id="70441-122">要使用的儲存空間帳戶名稱</span><span class="sxs-lookup"><span data-stu-id="70441-122">Name of the storage account to be used</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70441-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="70441-123">-PassThru</span></span>
<span data-ttu-id="70441-124">如果成功，則傳回 true</span><span class="sxs-lookup"><span data-stu-id="70441-124">returns true if successful</span></span>

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

### <span data-ttu-id="70441-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70441-125">-ResourceGroupName</span></span>
<span data-ttu-id="70441-126">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="70441-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70441-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="70441-127">-ResourceId</span></span>
<span data-ttu-id="70441-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="70441-128">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70441-129">-確認</span><span class="sxs-lookup"><span data-stu-id="70441-129">-Confirm</span></span>
<span data-ttu-id="70441-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="70441-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70441-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70441-131">-WhatIf</span></span>
<span data-ttu-id="70441-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="70441-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="70441-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="70441-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70441-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70441-134">CommonParameters</span></span>
<span data-ttu-id="70441-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="70441-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70441-136">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="70441-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70441-137">輸入</span><span class="sxs-lookup"><span data-stu-id="70441-137">INPUTS</span></span>

### <span data-ttu-id="70441-138">System.object</span><span class="sxs-lookup"><span data-stu-id="70441-138">System.String</span></span>

### <span data-ttu-id="70441-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="70441-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="70441-140">輸出</span><span class="sxs-lookup"><span data-stu-id="70441-140">OUTPUTS</span></span>

### <span data-ttu-id="70441-141">System.object</span><span class="sxs-lookup"><span data-stu-id="70441-141">System.Boolean</span></span>

## <span data-ttu-id="70441-142">筆記</span><span class="sxs-lookup"><span data-stu-id="70441-142">NOTES</span></span>

## <span data-ttu-id="70441-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="70441-143">RELATED LINKS</span></span>
