---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/enable-azdatalakestorekeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Enable-AzDataLakeStoreKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Enable-AzDataLakeStoreKeyVault.md
ms.openlocfilehash: 2b4b225ca050e3efedb1de1371006a4ffdb87587
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902090"
---
# <span data-ttu-id="fd71d-101">Enable-AzDataLakeStoreKeyVault</span><span class="sxs-lookup"><span data-stu-id="fd71d-101">Enable-AzDataLakeStoreKeyVault</span></span>

## <span data-ttu-id="fd71d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="fd71d-102">SYNOPSIS</span></span>
<span data-ttu-id="fd71d-103">嘗試啟用使用者管理的金鑰保存庫，以加密指定的 Data Lake Store 帳戶。</span><span class="sxs-lookup"><span data-stu-id="fd71d-103">Attempts to enable a user managed Key Vault for encryption of the specified Data Lake Store account.</span></span>

## <span data-ttu-id="fd71d-104">語法</span><span class="sxs-lookup"><span data-stu-id="fd71d-104">SYNTAX</span></span>

```
Enable-AzDataLakeStoreKeyVault [-Account] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd71d-105">描述</span><span class="sxs-lookup"><span data-stu-id="fd71d-105">DESCRIPTION</span></span>
<span data-ttu-id="fd71d-106">**Enable-AzDataLakeStoreKeyVault** Cmdlet 會嘗試啟用使用者管理的金鑰保存庫，以加密指定的 Data Lake Store 帳戶。</span><span class="sxs-lookup"><span data-stu-id="fd71d-106">The **Enable-AzDataLakeStoreKeyVault** cmdlet attempts to enable a user managed Key Vault for encryption of the specified Data Lake Store account.</span></span>

## <span data-ttu-id="fd71d-107">例子</span><span class="sxs-lookup"><span data-stu-id="fd71d-107">EXAMPLES</span></span>

### <span data-ttu-id="fd71d-108">範例 1：啟用 ContosoADLS 帳戶的金鑰庫</span><span class="sxs-lookup"><span data-stu-id="fd71d-108">Example 1: Enable the Key Vault for the ContosoADLS account</span></span>
```
PS C:\>Enable-AzDataLakeStoreKeyVault -Name "ContosoADLS"
```

<span data-ttu-id="fd71d-109">此命令會嘗試為名為 ContosoADLS 的 Data Lake Store 帳戶啟用使用者管理的金鑰保存庫。</span><span class="sxs-lookup"><span data-stu-id="fd71d-109">This command attempts to enable the user managed Key Vault for the Data Lake Store account named ContosoADLS.</span></span>

## <span data-ttu-id="fd71d-110">參數</span><span class="sxs-lookup"><span data-stu-id="fd71d-110">PARAMETERS</span></span>

### <span data-ttu-id="fd71d-111">-帳戶</span><span class="sxs-lookup"><span data-stu-id="fd71d-111">-Account</span></span>
<span data-ttu-id="fd71d-112">資料湖市集中帳戶，以啟用使用者管理的金鑰保存庫</span><span class="sxs-lookup"><span data-stu-id="fd71d-112">The Data Lake Store account to enable the user managed Key Vault for</span></span>

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

### <span data-ttu-id="fd71d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd71d-113">-DefaultProfile</span></span>
<span data-ttu-id="fd71d-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="fd71d-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fd71d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd71d-115">-ResourceGroupName</span></span>
<span data-ttu-id="fd71d-116">與帳戶相關聯的資源組名。</span><span class="sxs-lookup"><span data-stu-id="fd71d-116">Name of resource group associated with the account.</span></span> <span data-ttu-id="fd71d-117">如果未指定，將會嘗試進行發現。</span><span class="sxs-lookup"><span data-stu-id="fd71d-117">If not specified will attempt to be discovered.</span></span>

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

### <span data-ttu-id="fd71d-118">-確認</span><span class="sxs-lookup"><span data-stu-id="fd71d-118">-Confirm</span></span>
<span data-ttu-id="fd71d-119">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="fd71d-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd71d-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd71d-120">-WhatIf</span></span>
<span data-ttu-id="fd71d-121">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fd71d-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fd71d-122">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fd71d-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd71d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd71d-123">CommonParameters</span></span>
<span data-ttu-id="fd71d-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="fd71d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd71d-125">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="fd71d-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd71d-126">輸入</span><span class="sxs-lookup"><span data-stu-id="fd71d-126">INPUTS</span></span>

### <span data-ttu-id="fd71d-127">System.String</span><span class="sxs-lookup"><span data-stu-id="fd71d-127">System.String</span></span>

## <span data-ttu-id="fd71d-128">輸出</span><span class="sxs-lookup"><span data-stu-id="fd71d-128">OUTPUTS</span></span>

### <span data-ttu-id="fd71d-129">System.Void</span><span class="sxs-lookup"><span data-stu-id="fd71d-129">System.Void</span></span>

## <span data-ttu-id="fd71d-130">筆記</span><span class="sxs-lookup"><span data-stu-id="fd71d-130">NOTES</span></span>

## <span data-ttu-id="fd71d-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="fd71d-131">RELATED LINKS</span></span>

[<span data-ttu-id="fd71d-132">New-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="fd71d-132">New-AzDataLakeStoreAccount</span></span>](./New-AzDataLakeStoreAccount.md)

[<span data-ttu-id="fd71d-133">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="fd71d-133">Set-AzDataLakeStoreAccount</span></span>](./Set-AzDataLakeStoreAccount.md)

