---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/remove-aznetappfilesactivedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesActiveDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesActiveDirectory.md
ms.openlocfilehash: 9ab7607dd358e7c439539e99d44b263136f07cb4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906013"
---
# <span data-ttu-id="a6dd2-101">Remove-AzNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="a6dd2-101">Remove-AzNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="a6dd2-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a6dd2-102">SYNOPSIS</span></span>
<span data-ttu-id="a6dd2-103">刪除使用中目錄 (ANF) Azure NetApp 檔案。</span><span class="sxs-lookup"><span data-stu-id="a6dd2-103">Deletes an Azure NetApp Files (ANF) active directory configuration.</span></span>

## <span data-ttu-id="a6dd2-104">語法</span><span class="sxs-lookup"><span data-stu-id="a6dd2-104">SYNTAX</span></span>

### <span data-ttu-id="a6dd2-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="a6dd2-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesActiveDirectory -ResourceGroupName <String> -AccountName <String>
 -ActiveDirectoryId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a6dd2-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a6dd2-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesActiveDirectory -ActiveDirectoryId <String> -AccountObject <PSNetAppFilesAccount>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6dd2-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a6dd2-107">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesActiveDirectory -InputObject <PSNetAppFilesActiveDirectory> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6dd2-108">描述</span><span class="sxs-lookup"><span data-stu-id="a6dd2-108">DESCRIPTION</span></span>
<span data-ttu-id="a6dd2-109">**Remove-AzNetAppFilesActiveDirectory Cmdlet** 會刪除 ANF Active Directory 組式。</span><span class="sxs-lookup"><span data-stu-id="a6dd2-109">The **Remove-AzNetAppFilesActiveDirectory** cmdlet deletes an ANF active directory configuration.</span></span>

## <span data-ttu-id="a6dd2-110">例子</span><span class="sxs-lookup"><span data-stu-id="a6dd2-110">EXAMPLES</span></span>

### <span data-ttu-id="a6dd2-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="a6dd2-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzNetAppFilesActiveDirectory -ResourceGroupName "MyRG" -AccountName "MyAccount" -Name "MyADName"
```

<span data-ttu-id="a6dd2-112">此命令會刪除名稱為 「MyADName」的新 ANF Active Directory 組配置。</span><span class="sxs-lookup"><span data-stu-id="a6dd2-112">This command deletes the new ANF active directory configuration with a the name "MyADName".</span></span>

## <span data-ttu-id="a6dd2-113">參數</span><span class="sxs-lookup"><span data-stu-id="a6dd2-113">PARAMETERS</span></span>

### <span data-ttu-id="a6dd2-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a6dd2-114">-AccountName</span></span>
<span data-ttu-id="a6dd2-115">ANF 帳戶的名稱</span><span class="sxs-lookup"><span data-stu-id="a6dd2-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="a6dd2-116">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="a6dd2-116">-AccountObject</span></span>
<span data-ttu-id="a6dd2-117">Active Directory 物件的帳戶</span><span class="sxs-lookup"><span data-stu-id="a6dd2-117">The Account for the Active Directory object</span></span>

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

### <span data-ttu-id="a6dd2-118">-ActiveDirectoryId</span><span class="sxs-lookup"><span data-stu-id="a6dd2-118">-ActiveDirectoryId</span></span>
<span data-ttu-id="a6dd2-119">ANF Active Directory 的識別碼</span><span class="sxs-lookup"><span data-stu-id="a6dd2-119">The ID of the ANF active directory</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6dd2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6dd2-120">-DefaultProfile</span></span>
<span data-ttu-id="a6dd2-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a6dd2-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6dd2-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a6dd2-122">-InputObject</span></span>
<span data-ttu-id="a6dd2-123">要移除的 Active Directory 物件</span><span class="sxs-lookup"><span data-stu-id="a6dd2-123">The active directory object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a6dd2-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a6dd2-124">-PassThru</span></span>
<span data-ttu-id="a6dd2-125">返回指定的 Active Directory 是否已成功移除</span><span class="sxs-lookup"><span data-stu-id="a6dd2-125">Return whether the specified Active Directory  was successfully removed</span></span>

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

### <span data-ttu-id="a6dd2-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6dd2-126">-ResourceGroupName</span></span>
<span data-ttu-id="a6dd2-127">ANF 帳戶的資源群組</span><span class="sxs-lookup"><span data-stu-id="a6dd2-127">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="a6dd2-128">-確認</span><span class="sxs-lookup"><span data-stu-id="a6dd2-128">-Confirm</span></span>
<span data-ttu-id="a6dd2-129">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="a6dd2-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6dd2-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6dd2-130">-WhatIf</span></span>
<span data-ttu-id="a6dd2-131">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a6dd2-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6dd2-132">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a6dd2-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6dd2-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6dd2-133">CommonParameters</span></span>
<span data-ttu-id="a6dd2-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a6dd2-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6dd2-135">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a6dd2-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6dd2-136">輸入</span><span class="sxs-lookup"><span data-stu-id="a6dd2-136">INPUTS</span></span>

### <span data-ttu-id="a6dd2-137">Microsoft.Azure.Commands.NetAppFiles.models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="a6dd2-137">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="a6dd2-138">Microsoft.Azure.Commands.NetAppFiles.models.PSNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="a6dd2-138">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="a6dd2-139">輸出</span><span class="sxs-lookup"><span data-stu-id="a6dd2-139">OUTPUTS</span></span>

### <span data-ttu-id="a6dd2-140">Microsoft.Azure.Commands.NetAppFiles.models.PSNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="a6dd2-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="a6dd2-141">筆記</span><span class="sxs-lookup"><span data-stu-id="a6dd2-141">NOTES</span></span>

## <span data-ttu-id="a6dd2-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="a6dd2-142">RELATED LINKS</span></span>
