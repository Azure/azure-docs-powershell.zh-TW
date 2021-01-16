---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilesactivedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesActiveDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesActiveDirectory.md
ms.openlocfilehash: 7fcf1f749816872fb7407fedaea10d06f3385441
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98281753"
---
# <span data-ttu-id="dc8ad-101">Remove-AzNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="dc8ad-101">Remove-AzNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="dc8ad-102">摘要</span><span class="sxs-lookup"><span data-stu-id="dc8ad-102">SYNOPSIS</span></span>
<span data-ttu-id="dc8ad-103">刪除 (ANF) active directory 設定中的 Azure NetApp 檔案。</span><span class="sxs-lookup"><span data-stu-id="dc8ad-103">Deletes an Azure NetApp Files (ANF) active directory configuration.</span></span>

## <span data-ttu-id="dc8ad-104">句法</span><span class="sxs-lookup"><span data-stu-id="dc8ad-104">SYNTAX</span></span>

### <span data-ttu-id="dc8ad-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="dc8ad-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesActiveDirectory -ResourceGroupName <String> -AccountName <String>
 -ActiveDirectoryId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dc8ad-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc8ad-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesActiveDirectory -ActiveDirectoryId <String> -AccountObject <PSNetAppFilesAccount>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc8ad-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc8ad-107">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesActiveDirectory -InputObject <PSNetAppFilesActiveDirectory> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dc8ad-108">說明</span><span class="sxs-lookup"><span data-stu-id="dc8ad-108">DESCRIPTION</span></span>
<span data-ttu-id="dc8ad-109">**AzNetAppFilesActiveDirectory** Cmdlet 會刪除 ANF active directory 設定。</span><span class="sxs-lookup"><span data-stu-id="dc8ad-109">The **Remove-AzNetAppFilesActiveDirectory** cmdlet deletes an ANF active directory configuration.</span></span>

## <span data-ttu-id="dc8ad-110">示例</span><span class="sxs-lookup"><span data-stu-id="dc8ad-110">EXAMPLES</span></span>

### <span data-ttu-id="dc8ad-111">範例1</span><span class="sxs-lookup"><span data-stu-id="dc8ad-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzNetAppFilesActiveDirectory -ResourceGroupName "MyRG" -AccountName "MyAccount" -Name "MyADName"
```

<span data-ttu-id="dc8ad-112">這個命令會刪除新的 ANF active directory 設定，名稱為 "MyADName"。</span><span class="sxs-lookup"><span data-stu-id="dc8ad-112">This command deletes the new ANF active directory configuration with a the name "MyADName".</span></span>

## <span data-ttu-id="dc8ad-113">參數</span><span class="sxs-lookup"><span data-stu-id="dc8ad-113">PARAMETERS</span></span>

### <span data-ttu-id="dc8ad-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="dc8ad-114">-AccountName</span></span>
<span data-ttu-id="dc8ad-115">ANF 帳戶的名稱</span><span class="sxs-lookup"><span data-stu-id="dc8ad-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="dc8ad-116">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="dc8ad-116">-AccountObject</span></span>
<span data-ttu-id="dc8ad-117">Active Directory 物件的帳戶</span><span class="sxs-lookup"><span data-stu-id="dc8ad-117">The Account for the Active Directory object</span></span>

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

### <span data-ttu-id="dc8ad-118">-ActiveDirectoryId</span><span class="sxs-lookup"><span data-stu-id="dc8ad-118">-ActiveDirectoryId</span></span>
<span data-ttu-id="dc8ad-119">ANF active directory 的識別碼</span><span class="sxs-lookup"><span data-stu-id="dc8ad-119">The ID of the ANF active directory</span></span>

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

### <span data-ttu-id="dc8ad-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc8ad-120">-DefaultProfile</span></span>
<span data-ttu-id="dc8ad-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="dc8ad-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc8ad-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dc8ad-122">-InputObject</span></span>
<span data-ttu-id="dc8ad-123">要移除的 active directory 物件</span><span class="sxs-lookup"><span data-stu-id="dc8ad-123">The active directory object to remove</span></span>

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

### <span data-ttu-id="dc8ad-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dc8ad-124">-PassThru</span></span>
<span data-ttu-id="dc8ad-125">返回是否已成功移除指定的 Active Directory</span><span class="sxs-lookup"><span data-stu-id="dc8ad-125">Return whether the specified Active Directory  was successfully removed</span></span>

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

### <span data-ttu-id="dc8ad-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc8ad-126">-ResourceGroupName</span></span>
<span data-ttu-id="dc8ad-127">ANF 帳戶的 [資源] 群組</span><span class="sxs-lookup"><span data-stu-id="dc8ad-127">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="dc8ad-128">-確認</span><span class="sxs-lookup"><span data-stu-id="dc8ad-128">-Confirm</span></span>
<span data-ttu-id="dc8ad-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="dc8ad-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc8ad-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc8ad-130">-WhatIf</span></span>
<span data-ttu-id="dc8ad-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="dc8ad-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc8ad-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="dc8ad-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc8ad-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc8ad-133">CommonParameters</span></span>
<span data-ttu-id="dc8ad-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="dc8ad-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc8ad-135">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="dc8ad-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc8ad-136">輸入</span><span class="sxs-lookup"><span data-stu-id="dc8ad-136">INPUTS</span></span>

### <span data-ttu-id="dc8ad-137">PSNetAppFilesAccount 中的 NetAppFiles。</span><span class="sxs-lookup"><span data-stu-id="dc8ad-137">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="dc8ad-138">PSNetAppFilesActiveDirectory 中的 NetAppFiles。</span><span class="sxs-lookup"><span data-stu-id="dc8ad-138">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="dc8ad-139">輸出</span><span class="sxs-lookup"><span data-stu-id="dc8ad-139">OUTPUTS</span></span>

### <span data-ttu-id="dc8ad-140">PSNetAppFilesActiveDirectory 中的 NetAppFiles。</span><span class="sxs-lookup"><span data-stu-id="dc8ad-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="dc8ad-141">筆記</span><span class="sxs-lookup"><span data-stu-id="dc8ad-141">NOTES</span></span>

## <span data-ttu-id="dc8ad-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="dc8ad-142">RELATED LINKS</span></span>
