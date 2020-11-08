---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesPool.md
ms.openlocfilehash: 1ab6d38cc5401b4a7e813dafac933d6601a75acd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94138730"
---
# <span data-ttu-id="53a82-101">Remove-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="53a82-101">Remove-AzNetAppFilesPool</span></span>

## <span data-ttu-id="53a82-102">摘要</span><span class="sxs-lookup"><span data-stu-id="53a82-102">SYNOPSIS</span></span>
<span data-ttu-id="53a82-103">刪除 (ANF) 池的 Azure NetApp 檔案。</span><span class="sxs-lookup"><span data-stu-id="53a82-103">Deletes an Azure NetApp Files (ANF) pool.</span></span>

## <span data-ttu-id="53a82-104">句法</span><span class="sxs-lookup"><span data-stu-id="53a82-104">SYNTAX</span></span>

### <span data-ttu-id="53a82-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="53a82-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesPool -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53a82-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="53a82-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesPool -Name <String> -AccountObject <PSNetAppFilesAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53a82-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="53a82-107">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesPool -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53a82-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="53a82-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesPool -InputObject <PSNetAppFilesPool> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53a82-109">說明</span><span class="sxs-lookup"><span data-stu-id="53a82-109">DESCRIPTION</span></span>
<span data-ttu-id="53a82-110">**AzNetAppFilesPool** Cmdlet 會刪除 ANF 池。</span><span class="sxs-lookup"><span data-stu-id="53a82-110">The **Remove-AzNetAppFilesPool** cmdlet deletes an ANF pool.</span></span>

## <span data-ttu-id="53a82-111">示例</span><span class="sxs-lookup"><span data-stu-id="53a82-111">EXAMPLES</span></span>

### <span data-ttu-id="53a82-112">範例1</span><span class="sxs-lookup"><span data-stu-id="53a82-112">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesPool -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool"
```

<span data-ttu-id="53a82-113">這個命令會刪除 ANF 池子 "MyAnfPool"。</span><span class="sxs-lookup"><span data-stu-id="53a82-113">This command deletes the ANF pool "MyAnfPool".</span></span>

## <span data-ttu-id="53a82-114">參數</span><span class="sxs-lookup"><span data-stu-id="53a82-114">PARAMETERS</span></span>

### <span data-ttu-id="53a82-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="53a82-115">-AccountName</span></span>
<span data-ttu-id="53a82-116">ANF 帳戶的名稱</span><span class="sxs-lookup"><span data-stu-id="53a82-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="53a82-117">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="53a82-117">-AccountObject</span></span>
<span data-ttu-id="53a82-118">包含要移除之池的帳戶物件</span><span class="sxs-lookup"><span data-stu-id="53a82-118">The account object containing the pool to remove</span></span>

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

### <span data-ttu-id="53a82-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53a82-119">-DefaultProfile</span></span>
<span data-ttu-id="53a82-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="53a82-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53a82-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="53a82-121">-InputObject</span></span>
<span data-ttu-id="53a82-122">要移除的 pool 物件</span><span class="sxs-lookup"><span data-stu-id="53a82-122">The pool object to remove</span></span>

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

### <span data-ttu-id="53a82-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="53a82-123">-Name</span></span>
<span data-ttu-id="53a82-124">ANF 池的名稱</span><span class="sxs-lookup"><span data-stu-id="53a82-124">The name of the ANF pool</span></span>

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

### <span data-ttu-id="53a82-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="53a82-125">-PassThru</span></span>
<span data-ttu-id="53a82-126">傳回是否已成功移除指定的池</span><span class="sxs-lookup"><span data-stu-id="53a82-126">Return whether the specified pool was successfully removed</span></span>

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

### <span data-ttu-id="53a82-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53a82-127">-ResourceGroupName</span></span>
<span data-ttu-id="53a82-128">ANF 池的 [資源] 群組</span><span class="sxs-lookup"><span data-stu-id="53a82-128">The resource group of the ANF pool</span></span>

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

### <span data-ttu-id="53a82-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="53a82-129">-ResourceId</span></span>
<span data-ttu-id="53a82-130">ANF 池的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="53a82-130">The resource id of the ANF pool</span></span>

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

### <span data-ttu-id="53a82-131">-確認</span><span class="sxs-lookup"><span data-stu-id="53a82-131">-Confirm</span></span>
<span data-ttu-id="53a82-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="53a82-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53a82-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53a82-133">-WhatIf</span></span>
<span data-ttu-id="53a82-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="53a82-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53a82-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="53a82-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53a82-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53a82-136">CommonParameters</span></span>
<span data-ttu-id="53a82-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="53a82-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53a82-138">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="53a82-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53a82-139">輸入</span><span class="sxs-lookup"><span data-stu-id="53a82-139">INPUTS</span></span>

### <span data-ttu-id="53a82-140">System.object</span><span class="sxs-lookup"><span data-stu-id="53a82-140">System.String</span></span>

### <span data-ttu-id="53a82-141">PSNetAppFilesAccount 中的 NetAppFiles。</span><span class="sxs-lookup"><span data-stu-id="53a82-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="53a82-142">PSNetAppFilesPool 中的 NetAppFiles。</span><span class="sxs-lookup"><span data-stu-id="53a82-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="53a82-143">輸出</span><span class="sxs-lookup"><span data-stu-id="53a82-143">OUTPUTS</span></span>

### <span data-ttu-id="53a82-144">System.object</span><span class="sxs-lookup"><span data-stu-id="53a82-144">System.Boolean</span></span>

## <span data-ttu-id="53a82-145">筆記</span><span class="sxs-lookup"><span data-stu-id="53a82-145">NOTES</span></span>

## <span data-ttu-id="53a82-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="53a82-146">RELATED LINKS</span></span>
