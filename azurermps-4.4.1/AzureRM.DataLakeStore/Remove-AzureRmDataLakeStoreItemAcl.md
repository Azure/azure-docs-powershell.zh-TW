---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: D3E8A6A6-C6C5-46B0-914B-75088A6F6011
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreItemAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreItemAcl.md
ms.openlocfilehash: 48edcb93cb8fce66c9175bdcf498bd6545949090
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451720"
---
# <span data-ttu-id="012db-101">Remove-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="012db-101">Remove-AzureRmDataLakeStoreItemAcl</span></span>

## <span data-ttu-id="012db-102">摘要</span><span class="sxs-lookup"><span data-stu-id="012db-102">SYNOPSIS</span></span>
<span data-ttu-id="012db-103">清除 Data Lake Store 中的檔案或資料夾的 ACL。</span><span class="sxs-lookup"><span data-stu-id="012db-103">Clears the ACL of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="012db-104">句法</span><span class="sxs-lookup"><span data-stu-id="012db-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeStoreItemAcl [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Default] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="012db-105">說明</span><span class="sxs-lookup"><span data-stu-id="012db-105">DESCRIPTION</span></span>
<span data-ttu-id="012db-106">**AzureRmDataLakeStoreItemAcl** Cmdlet 會清除 Data Lake Store 中檔案或資料夾的存取控制清單 (ACL) 。</span><span class="sxs-lookup"><span data-stu-id="012db-106">The **Remove-AzureRmDataLakeStoreItemAcl** cmdlet clears the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="012db-107">示例</span><span class="sxs-lookup"><span data-stu-id="012db-107">EXAMPLES</span></span>

### <span data-ttu-id="012db-108">範例1：從資料夾移除 ACL</span><span class="sxs-lookup"><span data-stu-id="012db-108">Example 1: Remove the ACL from a folder</span></span>
```
PS C:\>Remove-AzureRmDataLakeStoreItemAcl -AccountName "ContosoADL" -Path "/"
```

<span data-ttu-id="012db-109">這個命令會移除 ContosoADL 帳戶根目錄的 ACL。</span><span class="sxs-lookup"><span data-stu-id="012db-109">This command removes the ACL for the root directory for the ContosoADL account.</span></span>

## <span data-ttu-id="012db-110">參數</span><span class="sxs-lookup"><span data-stu-id="012db-110">PARAMETERS</span></span>

### <span data-ttu-id="012db-111">-帳戶</span><span class="sxs-lookup"><span data-stu-id="012db-111">-Account</span></span>
<span data-ttu-id="012db-112">指定 Data Lake Store 帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="012db-112">Specifies the Data Lake Store account name.</span></span>

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

### <span data-ttu-id="012db-113">-預設值</span><span class="sxs-lookup"><span data-stu-id="012db-113">-Default</span></span>
<span data-ttu-id="012db-114">指示 Cmdlet 移除檔案或資料夾的預設 ACL。</span><span class="sxs-lookup"><span data-stu-id="012db-114">Indicates that the cmdlet removes the default ACL for a file or a folder.</span></span>

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

### <span data-ttu-id="012db-115">-Force</span><span class="sxs-lookup"><span data-stu-id="012db-115">-Force</span></span>
<span data-ttu-id="012db-116">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="012db-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="012db-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="012db-117">-PassThru</span></span>
<span data-ttu-id="012db-118">表示應傳回指示刪除操作結果的布林回應。</span><span class="sxs-lookup"><span data-stu-id="012db-118">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="012db-119">-Path</span><span class="sxs-lookup"><span data-stu-id="012db-119">-Path</span></span>
<span data-ttu-id="012db-120">指定專案的 Data Lake Store 路徑，從 root 目錄開始 (/) 。</span><span class="sxs-lookup"><span data-stu-id="012db-120">Specifies the Data Lake Store path of the item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="012db-121">-確認</span><span class="sxs-lookup"><span data-stu-id="012db-121">-Confirm</span></span>
<span data-ttu-id="012db-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="012db-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="012db-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="012db-123">-WhatIf</span></span>
<span data-ttu-id="012db-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="012db-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="012db-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="012db-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="012db-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="012db-126">-DefaultProfile</span></span>
<span data-ttu-id="012db-127">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="012db-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="012db-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="012db-128">CommonParameters</span></span>
<span data-ttu-id="012db-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="012db-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="012db-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="012db-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="012db-131">輸入</span><span class="sxs-lookup"><span data-stu-id="012db-131">INPUTS</span></span>

## <span data-ttu-id="012db-132">輸出</span><span class="sxs-lookup"><span data-stu-id="012db-132">OUTPUTS</span></span>

### <span data-ttu-id="012db-133">bool</span><span class="sxs-lookup"><span data-stu-id="012db-133">bool</span></span>
<span data-ttu-id="012db-134">如果已指定 PassThru，則會在成功完成時傳回 true。</span><span class="sxs-lookup"><span data-stu-id="012db-134">If PassThru is specified, returns true upon successful completion.</span></span>

## <span data-ttu-id="012db-135">筆記</span><span class="sxs-lookup"><span data-stu-id="012db-135">NOTES</span></span>
* <span data-ttu-id="012db-136">別名： Remove-AdlStoreAcl</span><span class="sxs-lookup"><span data-stu-id="012db-136">Alias: Remove-AdlStoreAcl</span></span>

## <span data-ttu-id="012db-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="012db-137">RELATED LINKS</span></span>

[<span data-ttu-id="012db-138">AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="012db-138">Get-AzureRmDataLakeStoreItemAclEntry</span></span>](./Get-AzureRmDataLakeStoreItemAclEntry.md)

[<span data-ttu-id="012db-139">Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="012db-139">Set-AzureRmDataLakeStoreItemAcl</span></span>](./Set-AzureRmDataLakeStoreItemAcl.md)

[<span data-ttu-id="012db-140">Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="012db-140">Set-AzureRmDataLakeStoreItemAclEntry</span></span>](./Set-AzureRmDataLakeStoreItemAclEntry.md)


