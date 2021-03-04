---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: D3E8A6A6-C6C5-46B0-914B-75088A6F6011
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/remove-azdatalakestoreitemacl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItemAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItemAcl.md
ms.openlocfilehash: 9b762a2fe0f12483fd664b8862e483b1b948bc75
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906705"
---
# <span data-ttu-id="7f931-101">Remove-AzDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="7f931-101">Remove-AzDataLakeStoreItemAcl</span></span>

## <span data-ttu-id="7f931-102">簡介</span><span class="sxs-lookup"><span data-stu-id="7f931-102">SYNOPSIS</span></span>
<span data-ttu-id="7f931-103">清除 Data Lake Store 中檔案或資料夾的 ACL。</span><span class="sxs-lookup"><span data-stu-id="7f931-103">Clears the ACL of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="7f931-104">語法</span><span class="sxs-lookup"><span data-stu-id="7f931-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreItemAcl [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Default] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f931-105">描述</span><span class="sxs-lookup"><span data-stu-id="7f931-105">DESCRIPTION</span></span>
<span data-ttu-id="7f931-106">**Remove-AzDataLakeStoreItemAcl** Cmdlet 會清除 Data Lake 市集 (檔案或資料夾的存取控制清單 (ACL) 。</span><span class="sxs-lookup"><span data-stu-id="7f931-106">The **Remove-AzDataLakeStoreItemAcl** cmdlet clears the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="7f931-107">例子</span><span class="sxs-lookup"><span data-stu-id="7f931-107">EXAMPLES</span></span>

### <span data-ttu-id="7f931-108">範例 1：從資料夾移除 ACL</span><span class="sxs-lookup"><span data-stu-id="7f931-108">Example 1: Remove the ACL from a folder</span></span>
```
PS C:\>Remove-AzDataLakeStoreItemAcl -AccountName "ContosoADL" -Path "/"
```

<span data-ttu-id="7f931-109">此命令會移除 ContosoADL 帳戶根目錄的 ACL。</span><span class="sxs-lookup"><span data-stu-id="7f931-109">This command removes the ACL for the root directory for the ContosoADL account.</span></span>

## <span data-ttu-id="7f931-110">參數</span><span class="sxs-lookup"><span data-stu-id="7f931-110">PARAMETERS</span></span>

### <span data-ttu-id="7f931-111">-帳戶</span><span class="sxs-lookup"><span data-stu-id="7f931-111">-Account</span></span>
<span data-ttu-id="7f931-112">指定 Data Lake Store 帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="7f931-112">Specifies the Data Lake Store account name.</span></span>

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

### <span data-ttu-id="7f931-113">-預設</span><span class="sxs-lookup"><span data-stu-id="7f931-113">-Default</span></span>
<span data-ttu-id="7f931-114">表示 Cmdlet 會移除檔案或資料夾的預設 ACL。</span><span class="sxs-lookup"><span data-stu-id="7f931-114">Indicates that the cmdlet removes the default ACL for a file or a folder.</span></span>

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

### <span data-ttu-id="7f931-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f931-115">-DefaultProfile</span></span>
<span data-ttu-id="7f931-116">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="7f931-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7f931-117">-強制</span><span class="sxs-lookup"><span data-stu-id="7f931-117">-Force</span></span>
<span data-ttu-id="7f931-118">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="7f931-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7f931-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7f931-119">-PassThru</span></span>
<span data-ttu-id="7f931-120">表示應該會返回布林值回應，指出刪除作業的結果。</span><span class="sxs-lookup"><span data-stu-id="7f931-120">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="7f931-121">-路徑</span><span class="sxs-lookup"><span data-stu-id="7f931-121">-Path</span></span>
<span data-ttu-id="7f931-122">指定專案的 Data Lake Store 路徑，從 / (根目錄開始) 。</span><span class="sxs-lookup"><span data-stu-id="7f931-122">Specifies the Data Lake Store path of the item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="7f931-123">-確認</span><span class="sxs-lookup"><span data-stu-id="7f931-123">-Confirm</span></span>
<span data-ttu-id="7f931-124">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="7f931-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f931-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f931-125">-WhatIf</span></span>
<span data-ttu-id="7f931-126">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7f931-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f931-127">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7f931-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f931-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f931-128">CommonParameters</span></span>
<span data-ttu-id="7f931-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="7f931-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f931-130">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="7f931-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f931-131">輸入</span><span class="sxs-lookup"><span data-stu-id="7f931-131">INPUTS</span></span>

### <span data-ttu-id="7f931-132">System.String</span><span class="sxs-lookup"><span data-stu-id="7f931-132">System.String</span></span>

### <span data-ttu-id="7f931-133">Microsoft.Azure.Commands.DataLakeStore.models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="7f931-133">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="7f931-134">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="7f931-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="7f931-135">輸出</span><span class="sxs-lookup"><span data-stu-id="7f931-135">OUTPUTS</span></span>

### <span data-ttu-id="7f931-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7f931-136">System.Boolean</span></span>

## <span data-ttu-id="7f931-137">筆記</span><span class="sxs-lookup"><span data-stu-id="7f931-137">NOTES</span></span>
* <span data-ttu-id="7f931-138">別名：Remove-AdlStoreAcl</span><span class="sxs-lookup"><span data-stu-id="7f931-138">Alias: Remove-AdlStoreAcl</span></span>

## <span data-ttu-id="7f931-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="7f931-139">RELATED LINKS</span></span>

[<span data-ttu-id="7f931-140">Get-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="7f931-140">Get-AzDataLakeStoreItemAclEntry</span></span>](./Get-AzDataLakeStoreItemAclEntry.md)

[<span data-ttu-id="7f931-141">Set-AzDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="7f931-141">Set-AzDataLakeStoreItemAcl</span></span>](./Set-AzDataLakeStoreItemAcl.md)

[<span data-ttu-id="7f931-142">Set-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="7f931-142">Set-AzDataLakeStoreItemAclEntry</span></span>](./Set-AzDataLakeStoreItemAclEntry.md)


