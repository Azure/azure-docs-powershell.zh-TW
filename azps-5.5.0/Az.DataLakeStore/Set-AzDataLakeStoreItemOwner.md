---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 415C5854-FE03-4D4E-BE84-408EA5F95E34
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestoreitemowner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemOwner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemOwner.md
ms.openlocfilehash: fc7c0e7ff8ef86b4a33f93e6b1286bb6e0baa00d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100136327"
---
# <span data-ttu-id="14b1d-101">Set-AzDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="14b1d-101">Set-AzDataLakeStoreItemOwner</span></span>

## <span data-ttu-id="14b1d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="14b1d-102">SYNOPSIS</span></span>
<span data-ttu-id="14b1d-103">修改 Data Lake Store 中的檔案或資料夾擁有者。</span><span class="sxs-lookup"><span data-stu-id="14b1d-103">Modifies the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="14b1d-104">句法</span><span class="sxs-lookup"><span data-stu-id="14b1d-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreItemOwner [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Type] <Owner>
 [-Id] <Guid> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="14b1d-105">說明</span><span class="sxs-lookup"><span data-stu-id="14b1d-105">DESCRIPTION</span></span>
<span data-ttu-id="14b1d-106">**AzDataLakeStoreItemOwner** Cmdlet 會修改 Data Lake store 中的檔案或資料夾擁有者。</span><span class="sxs-lookup"><span data-stu-id="14b1d-106">The **Set-AzDataLakeStoreItemOwner** cmdlet modifies the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="14b1d-107">示例</span><span class="sxs-lookup"><span data-stu-id="14b1d-107">EXAMPLES</span></span>

### <span data-ttu-id="14b1d-108">範例1：設定專案的擁有者</span><span class="sxs-lookup"><span data-stu-id="14b1d-108">Example 1: Set the owner for an item</span></span>
```
PS C:\>Set-AzDataLakeStoreItemOwner -AccountName "ContosoADL" -Path / -Type User -Id (Get-AzADUser -Mail "PattiFuller@contoso.com").ObjectId
```

<span data-ttu-id="14b1d-109">這個命令會將根目錄的擁有者設定為 Patti 更完整的目錄。</span><span class="sxs-lookup"><span data-stu-id="14b1d-109">This command sets the owner for the root directory to Patti Fuller.</span></span>

## <span data-ttu-id="14b1d-110">參數</span><span class="sxs-lookup"><span data-stu-id="14b1d-110">PARAMETERS</span></span>

### <span data-ttu-id="14b1d-111">-帳戶</span><span class="sxs-lookup"><span data-stu-id="14b1d-111">-Account</span></span>
<span data-ttu-id="14b1d-112">指定 Data Lake Store 帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="14b1d-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="14b1d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14b1d-113">-DefaultProfile</span></span>
<span data-ttu-id="14b1d-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="14b1d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="14b1d-115">-識別碼</span><span class="sxs-lookup"><span data-stu-id="14b1d-115">-Id</span></span>
<span data-ttu-id="14b1d-116">指定要作為擁有者使用之 AzureActive 目錄使用者、群組或服務主體的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="14b1d-116">Specifies the object ID of the AzureActive Directory user, group, or service principal to use as the owner.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14b1d-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="14b1d-117">-PassThru</span></span>
<span data-ttu-id="14b1d-118">指出應該傳回所產生的更新擁有者。</span><span class="sxs-lookup"><span data-stu-id="14b1d-118">Indicates the resulting updated owner should be returned.</span></span>

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

### <span data-ttu-id="14b1d-119">-Path</span><span class="sxs-lookup"><span data-stu-id="14b1d-119">-Path</span></span>
<span data-ttu-id="14b1d-120">指定要修改之專案的 Data Lake Store 路徑（從根目錄 (/) 開始）。</span><span class="sxs-lookup"><span data-stu-id="14b1d-120">Specifies the Data Lake Store path of the item to modify, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="14b1d-121">-類型</span><span class="sxs-lookup"><span data-stu-id="14b1d-121">-Type</span></span>
<span data-ttu-id="14b1d-122">指定要設定的擁有者類型。</span><span class="sxs-lookup"><span data-stu-id="14b1d-122">Specifies the type of owner to set.</span></span>
<span data-ttu-id="14b1d-123">此參數可接受的值為： [使用者] 和 [群組]。</span><span class="sxs-lookup"><span data-stu-id="14b1d-123">The acceptable values for this parameter are: User and Group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Owner
Parameter Sets: (All)
Aliases:
Accepted values: User, Group

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14b1d-124">-確認</span><span class="sxs-lookup"><span data-stu-id="14b1d-124">-Confirm</span></span>
<span data-ttu-id="14b1d-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="14b1d-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14b1d-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14b1d-126">-WhatIf</span></span>
<span data-ttu-id="14b1d-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="14b1d-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14b1d-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="14b1d-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14b1d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14b1d-129">CommonParameters</span></span>
<span data-ttu-id="14b1d-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="14b1d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14b1d-131">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="14b1d-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14b1d-132">輸入</span><span class="sxs-lookup"><span data-stu-id="14b1d-132">INPUTS</span></span>

### <span data-ttu-id="14b1d-133">System.object</span><span class="sxs-lookup"><span data-stu-id="14b1d-133">System.String</span></span>

### <span data-ttu-id="14b1d-134">DataLakeStorePathInstance 中的 DataLakeStore。</span><span class="sxs-lookup"><span data-stu-id="14b1d-134">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="14b1d-135">DataLakeStoreEnums + 擁有者 DataLakeStore。</span><span class="sxs-lookup"><span data-stu-id="14b1d-135">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Owner</span></span>

### <span data-ttu-id="14b1d-136">Guid.empty</span><span class="sxs-lookup"><span data-stu-id="14b1d-136">System.Guid</span></span>

### <span data-ttu-id="14b1d-137">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="14b1d-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="14b1d-138">輸出</span><span class="sxs-lookup"><span data-stu-id="14b1d-138">OUTPUTS</span></span>

### <span data-ttu-id="14b1d-139">System.object</span><span class="sxs-lookup"><span data-stu-id="14b1d-139">System.String</span></span>

## <span data-ttu-id="14b1d-140">筆記</span><span class="sxs-lookup"><span data-stu-id="14b1d-140">NOTES</span></span>

## <span data-ttu-id="14b1d-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="14b1d-141">RELATED LINKS</span></span>

[<span data-ttu-id="14b1d-142">AzDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="14b1d-142">Get-AzDataLakeStoreItemOwner</span></span>](./Get-AzDataLakeStoreItemOwner.md)


