---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeUser.md
ms.openlocfilehash: cecfa3e009f6d6fbc7167c4b8f1ca110d547b5b7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94128282"
---
# <span data-ttu-id="35c99-101">Remove-AzDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="35c99-101">Remove-AzDataBoxEdgeUser</span></span>

## <span data-ttu-id="35c99-102">摘要</span><span class="sxs-lookup"><span data-stu-id="35c99-102">SYNOPSIS</span></span>
<span data-ttu-id="35c99-103">移除裝置上的使用者。</span><span class="sxs-lookup"><span data-stu-id="35c99-103">Removes a user on a device.</span></span>

## <span data-ttu-id="35c99-104">句法</span><span class="sxs-lookup"><span data-stu-id="35c99-104">SYNTAX</span></span>

### <span data-ttu-id="35c99-105">DeleteByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="35c99-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35c99-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="35c99-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeUser [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35c99-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="35c99-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeUser [-InputObject] <PSDataBoxEdgeUser> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35c99-108">說明</span><span class="sxs-lookup"><span data-stu-id="35c99-108">DESCRIPTION</span></span>
<span data-ttu-id="35c99-109">**AzDataBoxEdgeUser** Cmdlet 會移除資料編輯方塊邊緣裝置上的使用者。</span><span class="sxs-lookup"><span data-stu-id="35c99-109">The **Remove-AzDataBoxEdgeUser** cmdlet removes a user on the Data Box Edge device.</span></span> <span data-ttu-id="35c99-110">只支援建立 type 類型的使用者 `Share` 。</span><span class="sxs-lookup"><span data-stu-id="35c99-110">Creation of only users of type `Share` is supported.</span></span>

## <span data-ttu-id="35c99-111">示例</span><span class="sxs-lookup"><span data-stu-id="35c99-111">EXAMPLES</span></span>

### <span data-ttu-id="35c99-112">範例1</span><span class="sxs-lookup"><span data-stu-id="35c99-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
```

## <span data-ttu-id="35c99-113">參數</span><span class="sxs-lookup"><span data-stu-id="35c99-113">PARAMETERS</span></span>

### <span data-ttu-id="35c99-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="35c99-114">-AsJob</span></span>
<span data-ttu-id="35c99-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="35c99-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="35c99-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35c99-116">-DefaultProfile</span></span>
<span data-ttu-id="35c99-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="35c99-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35c99-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="35c99-118">-DeviceName</span></span>
<span data-ttu-id="35c99-119">裝置名稱</span><span class="sxs-lookup"><span data-stu-id="35c99-119">Device Name</span></span>

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

### <span data-ttu-id="35c99-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="35c99-120">-InputObject</span></span>
<span data-ttu-id="35c99-121">輸入物件</span><span class="sxs-lookup"><span data-stu-id="35c99-121">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="35c99-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="35c99-122">-Name</span></span>
<span data-ttu-id="35c99-123">Username</span><span class="sxs-lookup"><span data-stu-id="35c99-123">Username</span></span>

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

### <span data-ttu-id="35c99-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="35c99-124">-PassThru</span></span>
<span data-ttu-id="35c99-125">如果成功，則傳回 true</span><span class="sxs-lookup"><span data-stu-id="35c99-125">returns true if successful</span></span>

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

### <span data-ttu-id="35c99-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35c99-126">-ResourceGroupName</span></span>
<span data-ttu-id="35c99-127">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="35c99-127">Resource Group Name</span></span>

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

### <span data-ttu-id="35c99-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="35c99-128">-ResourceId</span></span>
<span data-ttu-id="35c99-129">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="35c99-129">Azure ResourceId</span></span>

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

### <span data-ttu-id="35c99-130">-確認</span><span class="sxs-lookup"><span data-stu-id="35c99-130">-Confirm</span></span>
<span data-ttu-id="35c99-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="35c99-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35c99-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35c99-132">-WhatIf</span></span>
<span data-ttu-id="35c99-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="35c99-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="35c99-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="35c99-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35c99-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35c99-135">CommonParameters</span></span>
<span data-ttu-id="35c99-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="35c99-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35c99-137">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="35c99-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35c99-138">輸入</span><span class="sxs-lookup"><span data-stu-id="35c99-138">INPUTS</span></span>

### <span data-ttu-id="35c99-139">System.object</span><span class="sxs-lookup"><span data-stu-id="35c99-139">System.String</span></span>

### <span data-ttu-id="35c99-140">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="35c99-140">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span></span>

## <span data-ttu-id="35c99-141">輸出</span><span class="sxs-lookup"><span data-stu-id="35c99-141">OUTPUTS</span></span>

### <span data-ttu-id="35c99-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="35c99-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="35c99-143">筆記</span><span class="sxs-lookup"><span data-stu-id="35c99-143">NOTES</span></span>

## <span data-ttu-id="35c99-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="35c99-144">RELATED LINKS</span></span>
