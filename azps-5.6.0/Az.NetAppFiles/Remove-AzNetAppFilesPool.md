---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/remove-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesPool.md
ms.openlocfilehash: a62e6093ec5cfdf7244ea83b2dccf07ad07308fb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906002"
---
# <span data-ttu-id="c0e65-101">Remove-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="c0e65-101">Remove-AzNetAppFilesPool</span></span>

## <span data-ttu-id="c0e65-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c0e65-102">SYNOPSIS</span></span>
<span data-ttu-id="c0e65-103">刪除 ANF (中的 Azure NetApp 檔案) 檔案。</span><span class="sxs-lookup"><span data-stu-id="c0e65-103">Deletes an Azure NetApp Files (ANF) pool.</span></span>

## <span data-ttu-id="c0e65-104">語法</span><span class="sxs-lookup"><span data-stu-id="c0e65-104">SYNTAX</span></span>

### <span data-ttu-id="c0e65-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="c0e65-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesPool -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0e65-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c0e65-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesPool -Name <String> -AccountObject <PSNetAppFilesAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0e65-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c0e65-107">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesPool -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0e65-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c0e65-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesPool -InputObject <PSNetAppFilesPool> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0e65-109">描述</span><span class="sxs-lookup"><span data-stu-id="c0e65-109">DESCRIPTION</span></span>
<span data-ttu-id="c0e65-110">**Remove-AzNetAppFilesPool** Cmdlet 會刪除 ANF 資料庫。</span><span class="sxs-lookup"><span data-stu-id="c0e65-110">The **Remove-AzNetAppFilesPool** cmdlet deletes an ANF pool.</span></span>

## <span data-ttu-id="c0e65-111">例子</span><span class="sxs-lookup"><span data-stu-id="c0e65-111">EXAMPLES</span></span>

### <span data-ttu-id="c0e65-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="c0e65-112">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesPool -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool"
```

<span data-ttu-id="c0e65-113">此命令會刪除 ANF 資料庫 「MyAnfPool」。</span><span class="sxs-lookup"><span data-stu-id="c0e65-113">This command deletes the ANF pool "MyAnfPool".</span></span>

## <span data-ttu-id="c0e65-114">參數</span><span class="sxs-lookup"><span data-stu-id="c0e65-114">PARAMETERS</span></span>

### <span data-ttu-id="c0e65-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c0e65-115">-AccountName</span></span>
<span data-ttu-id="c0e65-116">ANF 帳戶的名稱</span><span class="sxs-lookup"><span data-stu-id="c0e65-116">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0e65-117">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="c0e65-117">-AccountObject</span></span>
<span data-ttu-id="c0e65-118">包含要移除之資料庫的帳戶物件</span><span class="sxs-lookup"><span data-stu-id="c0e65-118">The account object containing the pool to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c0e65-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0e65-119">-DefaultProfile</span></span>
<span data-ttu-id="c0e65-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="c0e65-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0e65-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c0e65-121">-InputObject</span></span>
<span data-ttu-id="c0e65-122">要移除的集中物件</span><span class="sxs-lookup"><span data-stu-id="c0e65-122">The pool object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c0e65-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="c0e65-123">-Name</span></span>
<span data-ttu-id="c0e65-124">ANF 組名</span><span class="sxs-lookup"><span data-stu-id="c0e65-124">The name of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: PoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0e65-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c0e65-125">-PassThru</span></span>
<span data-ttu-id="c0e65-126">返回指定的資料庫是否已成功移除</span><span class="sxs-lookup"><span data-stu-id="c0e65-126">Return whether the specified pool was successfully removed</span></span>

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

### <span data-ttu-id="c0e65-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0e65-127">-ResourceGroupName</span></span>
<span data-ttu-id="c0e65-128">ANF 資料庫的資源群組</span><span class="sxs-lookup"><span data-stu-id="c0e65-128">The resource group of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0e65-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c0e65-129">-ResourceId</span></span>
<span data-ttu-id="c0e65-130">ANF 資料庫的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="c0e65-130">The resource id of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0e65-131">-確認</span><span class="sxs-lookup"><span data-stu-id="c0e65-131">-Confirm</span></span>
<span data-ttu-id="c0e65-132">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="c0e65-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0e65-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0e65-133">-WhatIf</span></span>
<span data-ttu-id="c0e65-134">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c0e65-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0e65-135">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c0e65-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0e65-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0e65-136">CommonParameters</span></span>
<span data-ttu-id="c0e65-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c0e65-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0e65-138">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c0e65-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0e65-139">輸入</span><span class="sxs-lookup"><span data-stu-id="c0e65-139">INPUTS</span></span>

### <span data-ttu-id="c0e65-140">System.String</span><span class="sxs-lookup"><span data-stu-id="c0e65-140">System.String</span></span>

### <span data-ttu-id="c0e65-141">Microsoft.Azure.Commands.NetAppFiles.models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="c0e65-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="c0e65-142">Microsoft.Azure.Commands.NetAppFiles.models.PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="c0e65-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="c0e65-143">輸出</span><span class="sxs-lookup"><span data-stu-id="c0e65-143">OUTPUTS</span></span>

### <span data-ttu-id="c0e65-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c0e65-144">System.Boolean</span></span>

## <span data-ttu-id="c0e65-145">筆記</span><span class="sxs-lookup"><span data-stu-id="c0e65-145">NOTES</span></span>

## <span data-ttu-id="c0e65-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="c0e65-146">RELATED LINKS</span></span>
