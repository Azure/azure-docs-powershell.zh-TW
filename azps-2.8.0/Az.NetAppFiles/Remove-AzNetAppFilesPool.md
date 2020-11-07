---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesPool.md
ms.openlocfilehash: ef896185b606e107bb62208255a255655814fcbc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93789801"
---
# <span data-ttu-id="6b303-101">Remove-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="6b303-101">Remove-AzNetAppFilesPool</span></span>

## <span data-ttu-id="6b303-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6b303-102">SYNOPSIS</span></span>
<span data-ttu-id="6b303-103">刪除 (ANF) 池的 Azure NetApp 檔案。</span><span class="sxs-lookup"><span data-stu-id="6b303-103">Deletes an Azure NetApp Files (ANF) pool.</span></span>

## <span data-ttu-id="6b303-104">句法</span><span class="sxs-lookup"><span data-stu-id="6b303-104">SYNTAX</span></span>

### <span data-ttu-id="6b303-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="6b303-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesPool -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b303-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6b303-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesPool -Name <String> -AccountObject <PSNetAppFilesAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b303-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6b303-107">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesPool -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b303-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6b303-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesPool -InputObject <PSNetAppFilesPool> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b303-109">說明</span><span class="sxs-lookup"><span data-stu-id="6b303-109">DESCRIPTION</span></span>
<span data-ttu-id="6b303-110">**AzNetAppFilesPool** Cmdlet 會刪除 ANF 池。</span><span class="sxs-lookup"><span data-stu-id="6b303-110">The **Remove-AzNetAppFilesPool** cmdlet deletes an ANF pool.</span></span>

## <span data-ttu-id="6b303-111">示例</span><span class="sxs-lookup"><span data-stu-id="6b303-111">EXAMPLES</span></span>

### <span data-ttu-id="6b303-112">範例1</span><span class="sxs-lookup"><span data-stu-id="6b303-112">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesPool -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool"
```

<span data-ttu-id="6b303-113">這個命令會刪除 ANF 池子 "MyAnfPool"。</span><span class="sxs-lookup"><span data-stu-id="6b303-113">This command deletes the ANF pool "MyAnfPool".</span></span>

## <span data-ttu-id="6b303-114">參數</span><span class="sxs-lookup"><span data-stu-id="6b303-114">PARAMETERS</span></span>

### <span data-ttu-id="6b303-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="6b303-115">-AccountName</span></span>
<span data-ttu-id="6b303-116">ANF 帳戶的名稱</span><span class="sxs-lookup"><span data-stu-id="6b303-116">The name of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b303-117">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="6b303-117">-AccountObject</span></span>
<span data-ttu-id="6b303-118">包含要移除之池的帳戶物件</span><span class="sxs-lookup"><span data-stu-id="6b303-118">The account object containing the pool to remove</span></span>

```yaml
Type: PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6b303-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b303-119">-DefaultProfile</span></span>
<span data-ttu-id="6b303-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6b303-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b303-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6b303-121">-InputObject</span></span>
<span data-ttu-id="6b303-122">要移除的 pool 物件</span><span class="sxs-lookup"><span data-stu-id="6b303-122">The pool object to remove</span></span>

```yaml
Type: PSNetAppFilesPool
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6b303-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="6b303-123">-Name</span></span>
<span data-ttu-id="6b303-124">ANF 池的名稱</span><span class="sxs-lookup"><span data-stu-id="6b303-124">The name of the ANF pool</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: PoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b303-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6b303-125">-PassThru</span></span>
<span data-ttu-id="6b303-126">傳回是否已成功移除指定的池</span><span class="sxs-lookup"><span data-stu-id="6b303-126">Return whether the specified pool was successfully removed</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b303-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b303-127">-ResourceGroupName</span></span>
<span data-ttu-id="6b303-128">ANF 池的 [資源] 群組</span><span class="sxs-lookup"><span data-stu-id="6b303-128">The resource group of the ANF pool</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b303-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6b303-129">-ResourceId</span></span>
<span data-ttu-id="6b303-130">ANF 池的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="6b303-130">The resource id of the ANF pool</span></span>

```yaml
Type: String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b303-131">-確認</span><span class="sxs-lookup"><span data-stu-id="6b303-131">-Confirm</span></span>
<span data-ttu-id="6b303-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6b303-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b303-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b303-133">-WhatIf</span></span>
<span data-ttu-id="6b303-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6b303-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b303-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6b303-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b303-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b303-136">CommonParameters</span></span>
<span data-ttu-id="6b303-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6b303-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="6b303-138">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6b303-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b303-139">輸入</span><span class="sxs-lookup"><span data-stu-id="6b303-139">INPUTS</span></span>

### <span data-ttu-id="6b303-140">System.object</span><span class="sxs-lookup"><span data-stu-id="6b303-140">System.String</span></span>

### <span data-ttu-id="6b303-141">PSNetAppFilesAccount 中的 NetAppFiles。</span><span class="sxs-lookup"><span data-stu-id="6b303-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="6b303-142">PSNetAppFilesPool 中的 NetAppFiles。</span><span class="sxs-lookup"><span data-stu-id="6b303-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="6b303-143">輸出</span><span class="sxs-lookup"><span data-stu-id="6b303-143">OUTPUTS</span></span>

### <span data-ttu-id="6b303-144">System.object</span><span class="sxs-lookup"><span data-stu-id="6b303-144">System.Boolean</span></span>

## <span data-ttu-id="6b303-145">筆記</span><span class="sxs-lookup"><span data-stu-id="6b303-145">NOTES</span></span>

## <span data-ttu-id="6b303-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="6b303-146">RELATED LINKS</span></span>
