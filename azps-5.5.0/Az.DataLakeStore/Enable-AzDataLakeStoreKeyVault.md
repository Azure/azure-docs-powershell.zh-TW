---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/enable-azdatalakestorekeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Enable-AzDataLakeStoreKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Enable-AzDataLakeStoreKeyVault.md
ms.openlocfilehash: c6d15769891f02a6c1be12a277e17ca2ccba107e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100143275"
---
# <span data-ttu-id="f486f-101">Enable-AzDataLakeStoreKeyVault</span><span class="sxs-lookup"><span data-stu-id="f486f-101">Enable-AzDataLakeStoreKeyVault</span></span>

## <span data-ttu-id="f486f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f486f-102">SYNOPSIS</span></span>
<span data-ttu-id="f486f-103">嘗試啟用使用者管理的金鑰保存庫以加密指定的資料 Lake Store 帳戶。</span><span class="sxs-lookup"><span data-stu-id="f486f-103">Attempts to enable a user managed Key Vault for encryption of the specified Data Lake Store account.</span></span>

## <span data-ttu-id="f486f-104">句法</span><span class="sxs-lookup"><span data-stu-id="f486f-104">SYNTAX</span></span>

```
Enable-AzDataLakeStoreKeyVault [-Account] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f486f-105">說明</span><span class="sxs-lookup"><span data-stu-id="f486f-105">DESCRIPTION</span></span>
<span data-ttu-id="f486f-106">**Enable-AzDataLakeStoreKeyVault** Cmdlet 會嘗試啟用使用者管理的金鑰保存庫，以加密指定的資料 Lake store 帳戶。</span><span class="sxs-lookup"><span data-stu-id="f486f-106">The **Enable-AzDataLakeStoreKeyVault** cmdlet attempts to enable a user managed Key Vault for encryption of the specified Data Lake Store account.</span></span>

## <span data-ttu-id="f486f-107">示例</span><span class="sxs-lookup"><span data-stu-id="f486f-107">EXAMPLES</span></span>

### <span data-ttu-id="f486f-108">範例1：為 ContosoADLS 帳戶啟用金鑰保存庫</span><span class="sxs-lookup"><span data-stu-id="f486f-108">Example 1: Enable the Key Vault for the ContosoADLS account</span></span>
```
PS C:\>Enable-AzDataLakeStoreKeyVault -Name "ContosoADLS"
```

<span data-ttu-id="f486f-109">這個命令會嘗試針對名為 ContosoADLS 的 Data Lake Store 帳戶啟用使用者管理的金鑰保存庫。</span><span class="sxs-lookup"><span data-stu-id="f486f-109">This command attempts to enable the user managed Key Vault for the Data Lake Store account named ContosoADLS.</span></span>

## <span data-ttu-id="f486f-110">參數</span><span class="sxs-lookup"><span data-stu-id="f486f-110">PARAMETERS</span></span>

### <span data-ttu-id="f486f-111">-帳戶</span><span class="sxs-lookup"><span data-stu-id="f486f-111">-Account</span></span>
<span data-ttu-id="f486f-112">要啟用使用者管理的金鑰保存庫的 Data Lake Store 帳戶</span><span class="sxs-lookup"><span data-stu-id="f486f-112">The Data Lake Store account to enable the user managed Key Vault for</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f486f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f486f-113">-DefaultProfile</span></span>
<span data-ttu-id="f486f-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="f486f-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f486f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f486f-115">-ResourceGroupName</span></span>
<span data-ttu-id="f486f-116">與帳戶相關聯之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f486f-116">Name of resource group associated with the account.</span></span> <span data-ttu-id="f486f-117">如果未指定，將會嘗試探索。</span><span class="sxs-lookup"><span data-stu-id="f486f-117">If not specified will attempt to be discovered.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f486f-118">-確認</span><span class="sxs-lookup"><span data-stu-id="f486f-118">-Confirm</span></span>
<span data-ttu-id="f486f-119">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f486f-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f486f-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f486f-120">-WhatIf</span></span>
<span data-ttu-id="f486f-121">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f486f-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f486f-122">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f486f-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f486f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f486f-123">CommonParameters</span></span>
<span data-ttu-id="f486f-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f486f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f486f-125">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f486f-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f486f-126">輸入</span><span class="sxs-lookup"><span data-stu-id="f486f-126">INPUTS</span></span>

### <span data-ttu-id="f486f-127">System.object</span><span class="sxs-lookup"><span data-stu-id="f486f-127">System.String</span></span>

## <span data-ttu-id="f486f-128">輸出</span><span class="sxs-lookup"><span data-stu-id="f486f-128">OUTPUTS</span></span>

### <span data-ttu-id="f486f-129">System.void</span><span class="sxs-lookup"><span data-stu-id="f486f-129">System.Void</span></span>

## <span data-ttu-id="f486f-130">筆記</span><span class="sxs-lookup"><span data-stu-id="f486f-130">NOTES</span></span>

## <span data-ttu-id="f486f-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="f486f-131">RELATED LINKS</span></span>

[<span data-ttu-id="f486f-132">新-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="f486f-132">New-AzDataLakeStoreAccount</span></span>](./New-AzDataLakeStoreAccount.md)

[<span data-ttu-id="f486f-133">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="f486f-133">Set-AzDataLakeStoreAccount</span></span>](./Set-AzDataLakeStoreAccount.md)

