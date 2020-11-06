---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesAccount.md
ms.openlocfilehash: 5f59796a51ccd1f3e5e77442cde434ab803d0781
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93622213"
---
# <span data-ttu-id="815bd-101">Remove-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="815bd-101">Remove-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="815bd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="815bd-102">SYNOPSIS</span></span>
<span data-ttu-id="815bd-103">刪除 (ANF) 帳戶的 Azure NetApp 檔案。</span><span class="sxs-lookup"><span data-stu-id="815bd-103">Deletes an Azure NetApp Files (ANF) account.</span></span>

## <span data-ttu-id="815bd-104">句法</span><span class="sxs-lookup"><span data-stu-id="815bd-104">SYNTAX</span></span>

### <span data-ttu-id="815bd-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="815bd-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesAccount -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="815bd-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="815bd-106">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesAccount -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="815bd-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="815bd-107">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesAccount -InputObject <PSNetAppFilesAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="815bd-108">說明</span><span class="sxs-lookup"><span data-stu-id="815bd-108">DESCRIPTION</span></span>
<span data-ttu-id="815bd-109">**AzNetAppFilesAccount** Cmdlet 會刪除 ANF 帳戶。</span><span class="sxs-lookup"><span data-stu-id="815bd-109">The **Remove-AzNetAppFilesAccount** cmdlet deletes an ANF account.</span></span>

## <span data-ttu-id="815bd-110">示例</span><span class="sxs-lookup"><span data-stu-id="815bd-110">EXAMPLES</span></span>

### <span data-ttu-id="815bd-111">範例1</span><span class="sxs-lookup"><span data-stu-id="815bd-111">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesAccount -ResourceGroupName "MyRG" -Name "MyAnfAccount"
```

<span data-ttu-id="815bd-112">這個命令會刪除 ANF 帳戶 "MyAnfAccount"。</span><span class="sxs-lookup"><span data-stu-id="815bd-112">This command deletes the ANF account "MyAnfAccount".</span></span>

## <span data-ttu-id="815bd-113">參數</span><span class="sxs-lookup"><span data-stu-id="815bd-113">PARAMETERS</span></span>

### <span data-ttu-id="815bd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="815bd-114">-DefaultProfile</span></span>
<span data-ttu-id="815bd-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="815bd-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="815bd-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="815bd-116">-InputObject</span></span>
<span data-ttu-id="815bd-117">要移除的帳戶物件</span><span class="sxs-lookup"><span data-stu-id="815bd-117">The account object to remove</span></span>

```yaml
Type: PSNetAppFilesAccount
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="815bd-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="815bd-118">-Name</span></span>
<span data-ttu-id="815bd-119">ANF 帳戶的名稱</span><span class="sxs-lookup"><span data-stu-id="815bd-119">The name of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="815bd-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="815bd-120">-PassThru</span></span>
<span data-ttu-id="815bd-121">返回是否已成功移除指定的帳號</span><span class="sxs-lookup"><span data-stu-id="815bd-121">Return whether the specified account was successfully removed</span></span>

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

### <span data-ttu-id="815bd-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="815bd-122">-ResourceGroupName</span></span>
<span data-ttu-id="815bd-123">ANF 帳戶的 [資源] 群組</span><span class="sxs-lookup"><span data-stu-id="815bd-123">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="815bd-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="815bd-124">-ResourceId</span></span>
<span data-ttu-id="815bd-125">ANF 帳戶的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="815bd-125">The resource id of the ANF account</span></span>

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

### <span data-ttu-id="815bd-126">-確認</span><span class="sxs-lookup"><span data-stu-id="815bd-126">-Confirm</span></span>
<span data-ttu-id="815bd-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="815bd-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="815bd-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="815bd-128">-WhatIf</span></span>
<span data-ttu-id="815bd-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="815bd-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="815bd-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="815bd-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="815bd-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="815bd-131">CommonParameters</span></span>
<span data-ttu-id="815bd-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="815bd-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="815bd-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="815bd-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="815bd-134">輸入</span><span class="sxs-lookup"><span data-stu-id="815bd-134">INPUTS</span></span>

### <span data-ttu-id="815bd-135">System.object</span><span class="sxs-lookup"><span data-stu-id="815bd-135">System.String</span></span>

### <span data-ttu-id="815bd-136">PSNetAppFilesAccount 中的 NetAppFiles。</span><span class="sxs-lookup"><span data-stu-id="815bd-136">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="815bd-137">輸出</span><span class="sxs-lookup"><span data-stu-id="815bd-137">OUTPUTS</span></span>

### <span data-ttu-id="815bd-138">System.object</span><span class="sxs-lookup"><span data-stu-id="815bd-138">System.Boolean</span></span>

## <span data-ttu-id="815bd-139">筆記</span><span class="sxs-lookup"><span data-stu-id="815bd-139">NOTES</span></span>

## <span data-ttu-id="815bd-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="815bd-140">RELATED LINKS</span></span>
