---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: D3E8A6A6-C6C5-46B0-914B-75088A6F6011
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/remove-azdatalakestoreitemacl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItemAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItemAcl.md
ms.openlocfilehash: 9339857a125ca0646869a81749f9cf55ff2531ee
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93612763"
---
# <span data-ttu-id="b459e-101">Remove-AzDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="b459e-101">Remove-AzDataLakeStoreItemAcl</span></span>

## <span data-ttu-id="b459e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b459e-102">SYNOPSIS</span></span>
<span data-ttu-id="b459e-103">清除 Data Lake Store 中的檔案或資料夾的 ACL。</span><span class="sxs-lookup"><span data-stu-id="b459e-103">Clears the ACL of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="b459e-104">句法</span><span class="sxs-lookup"><span data-stu-id="b459e-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreItemAcl [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Default] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b459e-105">說明</span><span class="sxs-lookup"><span data-stu-id="b459e-105">DESCRIPTION</span></span>
<span data-ttu-id="b459e-106">**AzDataLakeStoreItemAcl** Cmdlet 會清除 Data Lake Store 中檔案或資料夾的存取控制清單 (ACL) 。</span><span class="sxs-lookup"><span data-stu-id="b459e-106">The **Remove-AzDataLakeStoreItemAcl** cmdlet clears the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="b459e-107">示例</span><span class="sxs-lookup"><span data-stu-id="b459e-107">EXAMPLES</span></span>

### <span data-ttu-id="b459e-108">範例1：從資料夾移除 ACL</span><span class="sxs-lookup"><span data-stu-id="b459e-108">Example 1: Remove the ACL from a folder</span></span>
```
PS C:\>Remove-AzDataLakeStoreItemAcl -AccountName "ContosoADL" -Path "/"
```

<span data-ttu-id="b459e-109">這個命令會移除 ContosoADL 帳戶根目錄的 ACL。</span><span class="sxs-lookup"><span data-stu-id="b459e-109">This command removes the ACL for the root directory for the ContosoADL account.</span></span>

## <span data-ttu-id="b459e-110">參數</span><span class="sxs-lookup"><span data-stu-id="b459e-110">PARAMETERS</span></span>

### <span data-ttu-id="b459e-111">-帳戶</span><span class="sxs-lookup"><span data-stu-id="b459e-111">-Account</span></span>
<span data-ttu-id="b459e-112">指定 Data Lake Store 帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="b459e-112">Specifies the Data Lake Store account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b459e-113">-預設值</span><span class="sxs-lookup"><span data-stu-id="b459e-113">-Default</span></span>
<span data-ttu-id="b459e-114">指示 Cmdlet 移除檔案或資料夾的預設 ACL。</span><span class="sxs-lookup"><span data-stu-id="b459e-114">Indicates that the cmdlet removes the default ACL for a file or a folder.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b459e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b459e-115">-DefaultProfile</span></span>
<span data-ttu-id="b459e-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b459e-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b459e-117">-Force</span><span class="sxs-lookup"><span data-stu-id="b459e-117">-Force</span></span>
<span data-ttu-id="b459e-118">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="b459e-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b459e-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b459e-119">-PassThru</span></span>
<span data-ttu-id="b459e-120">表示應傳回指示刪除操作結果的布林回應。</span><span class="sxs-lookup"><span data-stu-id="b459e-120">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="b459e-121">-Path</span><span class="sxs-lookup"><span data-stu-id="b459e-121">-Path</span></span>
<span data-ttu-id="b459e-122">指定專案的 Data Lake Store 路徑，從 root 目錄開始 (/) 。</span><span class="sxs-lookup"><span data-stu-id="b459e-122">Specifies the Data Lake Store path of the item, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b459e-123">-確認</span><span class="sxs-lookup"><span data-stu-id="b459e-123">-Confirm</span></span>
<span data-ttu-id="b459e-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b459e-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b459e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b459e-125">-WhatIf</span></span>
<span data-ttu-id="b459e-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b459e-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b459e-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b459e-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b459e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b459e-128">CommonParameters</span></span>
<span data-ttu-id="b459e-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b459e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b459e-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b459e-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b459e-131">輸入</span><span class="sxs-lookup"><span data-stu-id="b459e-131">INPUTS</span></span>

### <span data-ttu-id="b459e-132">System.object</span><span class="sxs-lookup"><span data-stu-id="b459e-132">System.String</span></span>

### <span data-ttu-id="b459e-133">DataLakeStorePathInstance 中的 DataLakeStore。</span><span class="sxs-lookup"><span data-stu-id="b459e-133">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="b459e-134">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="b459e-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b459e-135">輸出</span><span class="sxs-lookup"><span data-stu-id="b459e-135">OUTPUTS</span></span>

### <span data-ttu-id="b459e-136">System.object</span><span class="sxs-lookup"><span data-stu-id="b459e-136">System.Boolean</span></span>

## <span data-ttu-id="b459e-137">筆記</span><span class="sxs-lookup"><span data-stu-id="b459e-137">NOTES</span></span>
* <span data-ttu-id="b459e-138">別名： Remove-AdlStoreAcl</span><span class="sxs-lookup"><span data-stu-id="b459e-138">Alias: Remove-AdlStoreAcl</span></span>

## <span data-ttu-id="b459e-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="b459e-139">RELATED LINKS</span></span>

[<span data-ttu-id="b459e-140">AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="b459e-140">Get-AzDataLakeStoreItemAclEntry</span></span>](./Get-AzDataLakeStoreItemAclEntry.md)

[<span data-ttu-id="b459e-141">Set-AzDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="b459e-141">Set-AzDataLakeStoreItemAcl</span></span>](./Set-AzDataLakeStoreItemAcl.md)

[<span data-ttu-id="b459e-142">Set-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="b459e-142">Set-AzDataLakeStoreItemAclEntry</span></span>](./Set-AzDataLakeStoreItemAclEntry.md)


