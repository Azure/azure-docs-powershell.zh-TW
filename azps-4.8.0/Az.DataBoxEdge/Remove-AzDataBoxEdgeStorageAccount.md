---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgestorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeStorageAccount.md
ms.openlocfilehash: 1f8e20b826a477778de5325ff147cbd7ad28a9fb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94135631"
---
# <span data-ttu-id="846bd-101">Remove-AzDataBoxEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="846bd-101">Remove-AzDataBoxEdgeStorageAccount</span></span>

## <span data-ttu-id="846bd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="846bd-102">SYNOPSIS</span></span>
<span data-ttu-id="846bd-103">移除裝置的邊緣儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="846bd-103">Removes the Edge Storage account for a device.</span></span>

## <span data-ttu-id="846bd-104">句法</span><span class="sxs-lookup"><span data-stu-id="846bd-104">SYNTAX</span></span>

### <span data-ttu-id="846bd-105">DeleteByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="846bd-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="846bd-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="846bd-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeStorageAccount [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="846bd-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="846bd-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeStorageAccount [-InputObject] <PSDataBoxEdgeStorageAccount> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="846bd-108">說明</span><span class="sxs-lookup"><span data-stu-id="846bd-108">DESCRIPTION</span></span>
<span data-ttu-id="846bd-109">**AzDataBoxEdgeStorageAccount** Cmdlet 會移除資料盒 edge 裝置的關聯邊緣儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="846bd-109">The **Remove-AzDataBoxEdgeStorageAccount** cmdlet removes an associated Edge Storage Account for a Data Box Edge device.</span></span> <span data-ttu-id="846bd-110">您可以指定要移除為 Cmdlet 中的參數的 Edge 儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="846bd-110">You can specify the name of the Edge Storage Account to be removed as a parameter in the cmdlet.</span></span>

## <span data-ttu-id="846bd-111">示例</span><span class="sxs-lookup"><span data-stu-id="846bd-111">EXAMPLES</span></span>

### <span data-ttu-id="846bd-112">範例1</span><span class="sxs-lookup"><span data-stu-id="846bd-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeStorageAccount -ResourceGroupName resourceGroupName -DeviceName deviceName -Name edgestorageaccountname
```

## <span data-ttu-id="846bd-113">參數</span><span class="sxs-lookup"><span data-stu-id="846bd-113">PARAMETERS</span></span>

### <span data-ttu-id="846bd-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="846bd-114">-AsJob</span></span>
<span data-ttu-id="846bd-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="846bd-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="846bd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="846bd-116">-DefaultProfile</span></span>
<span data-ttu-id="846bd-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="846bd-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="846bd-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="846bd-118">-DeviceName</span></span>
<span data-ttu-id="846bd-119">裝置名稱</span><span class="sxs-lookup"><span data-stu-id="846bd-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="846bd-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="846bd-120">-InputObject</span></span>
<span data-ttu-id="846bd-121">輸入物件</span><span class="sxs-lookup"><span data-stu-id="846bd-121">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="846bd-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="846bd-122">-Name</span></span>
<span data-ttu-id="846bd-123">資源名稱</span><span class="sxs-lookup"><span data-stu-id="846bd-123">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="846bd-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="846bd-124">-PassThru</span></span>
<span data-ttu-id="846bd-125">如果成功，則傳回 true</span><span class="sxs-lookup"><span data-stu-id="846bd-125">returns true if successful</span></span>

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

### <span data-ttu-id="846bd-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="846bd-126">-ResourceGroupName</span></span>
<span data-ttu-id="846bd-127">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="846bd-127">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="846bd-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="846bd-128">-ResourceId</span></span>
<span data-ttu-id="846bd-129">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="846bd-129">Azure ResourceId</span></span>

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

### <span data-ttu-id="846bd-130">-確認</span><span class="sxs-lookup"><span data-stu-id="846bd-130">-Confirm</span></span>
<span data-ttu-id="846bd-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="846bd-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="846bd-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="846bd-132">-WhatIf</span></span>
<span data-ttu-id="846bd-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="846bd-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="846bd-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="846bd-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="846bd-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="846bd-135">CommonParameters</span></span>
<span data-ttu-id="846bd-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="846bd-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="846bd-137">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="846bd-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="846bd-138">輸入</span><span class="sxs-lookup"><span data-stu-id="846bd-138">INPUTS</span></span>

### <span data-ttu-id="846bd-139">System.object</span><span class="sxs-lookup"><span data-stu-id="846bd-139">System.String</span></span>

### <span data-ttu-id="846bd-140">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="846bd-140">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span></span>

## <span data-ttu-id="846bd-141">輸出</span><span class="sxs-lookup"><span data-stu-id="846bd-141">OUTPUTS</span></span>

### <span data-ttu-id="846bd-142">System.object</span><span class="sxs-lookup"><span data-stu-id="846bd-142">System.Boolean</span></span>

## <span data-ttu-id="846bd-143">筆記</span><span class="sxs-lookup"><span data-stu-id="846bd-143">NOTES</span></span>

## <span data-ttu-id="846bd-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="846bd-144">RELATED LINKS</span></span>