---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: D3E8A6A6-C6C5-46B0-914B-75088A6F6011
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/remove-azurermdatalakestoreitemacl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreItemAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreItemAcl.md
ms.openlocfilehash: e1be38957ba7ca91a275031e6e076efb410f7acb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93443867"
---
# <span data-ttu-id="52b68-101">Remove-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="52b68-101">Remove-AzureRmDataLakeStoreItemAcl</span></span>

## <span data-ttu-id="52b68-102">摘要</span><span class="sxs-lookup"><span data-stu-id="52b68-102">SYNOPSIS</span></span>
<span data-ttu-id="52b68-103">清除 Data Lake Store 中的檔案或資料夾的 ACL。</span><span class="sxs-lookup"><span data-stu-id="52b68-103">Clears the ACL of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="52b68-104">句法</span><span class="sxs-lookup"><span data-stu-id="52b68-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeStoreItemAcl [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Default] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52b68-105">說明</span><span class="sxs-lookup"><span data-stu-id="52b68-105">DESCRIPTION</span></span>
<span data-ttu-id="52b68-106">**AzureRmDataLakeStoreItemAcl** Cmdlet 會清除 Data Lake Store 中檔案或資料夾的存取控制清單 (ACL) 。</span><span class="sxs-lookup"><span data-stu-id="52b68-106">The **Remove-AzureRmDataLakeStoreItemAcl** cmdlet clears the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="52b68-107">示例</span><span class="sxs-lookup"><span data-stu-id="52b68-107">EXAMPLES</span></span>

### <span data-ttu-id="52b68-108">範例1：從資料夾移除 ACL</span><span class="sxs-lookup"><span data-stu-id="52b68-108">Example 1: Remove the ACL from a folder</span></span>
```
PS C:\>Remove-AzureRmDataLakeStoreItemAcl -AccountName "ContosoADL" -Path "/"
```

<span data-ttu-id="52b68-109">這個命令會移除 ContosoADL 帳戶根目錄的 ACL。</span><span class="sxs-lookup"><span data-stu-id="52b68-109">This command removes the ACL for the root directory for the ContosoADL account.</span></span>

## <span data-ttu-id="52b68-110">參數</span><span class="sxs-lookup"><span data-stu-id="52b68-110">PARAMETERS</span></span>

### <span data-ttu-id="52b68-111">-帳戶</span><span class="sxs-lookup"><span data-stu-id="52b68-111">-Account</span></span>
<span data-ttu-id="52b68-112">指定 Data Lake Store 帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="52b68-112">Specifies the Data Lake Store account name.</span></span>

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

### <span data-ttu-id="52b68-113">-預設值</span><span class="sxs-lookup"><span data-stu-id="52b68-113">-Default</span></span>
<span data-ttu-id="52b68-114">指示 Cmdlet 移除檔案或資料夾的預設 ACL。</span><span class="sxs-lookup"><span data-stu-id="52b68-114">Indicates that the cmdlet removes the default ACL for a file or a folder.</span></span>

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

### <span data-ttu-id="52b68-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52b68-115">-DefaultProfile</span></span>
<span data-ttu-id="52b68-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="52b68-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52b68-117">-Force</span><span class="sxs-lookup"><span data-stu-id="52b68-117">-Force</span></span>
<span data-ttu-id="52b68-118">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="52b68-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="52b68-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="52b68-119">-PassThru</span></span>
<span data-ttu-id="52b68-120">表示應傳回指示刪除操作結果的布林回應。</span><span class="sxs-lookup"><span data-stu-id="52b68-120">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="52b68-121">-Path</span><span class="sxs-lookup"><span data-stu-id="52b68-121">-Path</span></span>
<span data-ttu-id="52b68-122">指定專案的 Data Lake Store 路徑，從 root 目錄開始 (/) 。</span><span class="sxs-lookup"><span data-stu-id="52b68-122">Specifies the Data Lake Store path of the item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="52b68-123">-確認</span><span class="sxs-lookup"><span data-stu-id="52b68-123">-Confirm</span></span>
<span data-ttu-id="52b68-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="52b68-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52b68-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52b68-125">-WhatIf</span></span>
<span data-ttu-id="52b68-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="52b68-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52b68-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="52b68-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52b68-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52b68-128">CommonParameters</span></span>
<span data-ttu-id="52b68-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="52b68-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52b68-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="52b68-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52b68-131">輸入</span><span class="sxs-lookup"><span data-stu-id="52b68-131">INPUTS</span></span>

### <span data-ttu-id="52b68-132">System.object</span><span class="sxs-lookup"><span data-stu-id="52b68-132">System.String</span></span>

### <span data-ttu-id="52b68-133">DataLakeStorePathInstance 中的 DataLakeStore。</span><span class="sxs-lookup"><span data-stu-id="52b68-133">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="52b68-134">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="52b68-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="52b68-135">輸出</span><span class="sxs-lookup"><span data-stu-id="52b68-135">OUTPUTS</span></span>

### <span data-ttu-id="52b68-136">System.object</span><span class="sxs-lookup"><span data-stu-id="52b68-136">System.Boolean</span></span>

## <span data-ttu-id="52b68-137">筆記</span><span class="sxs-lookup"><span data-stu-id="52b68-137">NOTES</span></span>
* <span data-ttu-id="52b68-138">別名： Remove-AdlStoreAcl</span><span class="sxs-lookup"><span data-stu-id="52b68-138">Alias: Remove-AdlStoreAcl</span></span>

## <span data-ttu-id="52b68-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="52b68-139">RELATED LINKS</span></span>

[<span data-ttu-id="52b68-140">AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="52b68-140">Get-AzureRmDataLakeStoreItemAclEntry</span></span>](./Get-AzureRmDataLakeStoreItemAclEntry.md)

[<span data-ttu-id="52b68-141">Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="52b68-141">Set-AzureRmDataLakeStoreItemAcl</span></span>](./Set-AzureRmDataLakeStoreItemAcl.md)

[<span data-ttu-id="52b68-142">Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="52b68-142">Set-AzureRmDataLakeStoreItemAclEntry</span></span>](./Set-AzureRmDataLakeStoreItemAclEntry.md)


