---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 30C10687-F172-4663-8D4A-F0DDEA5C3741
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/remove-azdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: d8762d0ddd689d40397bee423e8166aa8dd7a6a1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904502"
---
# <span data-ttu-id="7ab6f-101">Remove-AzDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="7ab6f-101">Remove-AzDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="7ab6f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="7ab6f-102">SYNOPSIS</span></span>
<span data-ttu-id="7ab6f-103">移除指定 Data Lake Store 中指定的信任身分識別提供者。</span><span class="sxs-lookup"><span data-stu-id="7ab6f-103">Removes the specified trusted identity provider in the specified Data Lake Store.</span></span>

## <span data-ttu-id="7ab6f-104">語法</span><span class="sxs-lookup"><span data-stu-id="7ab6f-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreTrustedIdProvider [-Account] <String> [[-Name] <String>] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7ab6f-105">描述</span><span class="sxs-lookup"><span data-stu-id="7ab6f-105">DESCRIPTION</span></span>
<span data-ttu-id="7ab6f-106">**Remove-AzDataLakeStoreTrustedIdProvider Cmdlet** 會移除指定 Data Lake Store 中指定的信任身分識別提供者。</span><span class="sxs-lookup"><span data-stu-id="7ab6f-106">The **Remove-AzDataLakeStoreTrustedIdProvider** cmdlet removes the specified trusted identity provider in the specified Data Lake Store.</span></span>

## <span data-ttu-id="7ab6f-107">例子</span><span class="sxs-lookup"><span data-stu-id="7ab6f-107">EXAMPLES</span></span>

### <span data-ttu-id="7ab6f-108">範例 1：移除信任的身分識別提供者。</span><span class="sxs-lookup"><span data-stu-id="7ab6f-108">Example 1: Remove a trusted identity provider.</span></span>
```
PS C:\> Remove-AzDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider
```

<span data-ttu-id="7ab6f-109">從帳戶 "ContosoADL" 移除提供者 "MyProvider"</span><span class="sxs-lookup"><span data-stu-id="7ab6f-109">Removes the provider "MyProvider" from account "ContosoADL"</span></span>

## <span data-ttu-id="7ab6f-110">參數</span><span class="sxs-lookup"><span data-stu-id="7ab6f-110">PARAMETERS</span></span>

### <span data-ttu-id="7ab6f-111">-帳戶</span><span class="sxs-lookup"><span data-stu-id="7ab6f-111">-Account</span></span>
<span data-ttu-id="7ab6f-112">若要移除信任的身分識別提供者，請從 Data Lake Store 帳戶移除</span><span class="sxs-lookup"><span data-stu-id="7ab6f-112">The Data Lake Store account to remove the trusted identity provider from</span></span>

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

### <span data-ttu-id="7ab6f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ab6f-113">-DefaultProfile</span></span>
<span data-ttu-id="7ab6f-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="7ab6f-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7ab6f-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="7ab6f-115">-Name</span></span>
<span data-ttu-id="7ab6f-116">信任的身分識別提供者的名稱。</span><span class="sxs-lookup"><span data-stu-id="7ab6f-116">The name of the trusted identity provider.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ab6f-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7ab6f-117">-PassThru</span></span>
<span data-ttu-id="7ab6f-118">表示應該會返回布林值回應，指出刪除作業的結果。</span><span class="sxs-lookup"><span data-stu-id="7ab6f-118">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="7ab6f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ab6f-119">-ResourceGroupName</span></span>
<span data-ttu-id="7ab6f-120">指定包含帳戶的資源組名，以移除信任的身分識別提供者。</span><span class="sxs-lookup"><span data-stu-id="7ab6f-120">Specifies the name of the resource group that contains the account to remove the trusted identity provider from.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ab6f-121">-確認</span><span class="sxs-lookup"><span data-stu-id="7ab6f-121">-Confirm</span></span>
<span data-ttu-id="7ab6f-122">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="7ab6f-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ab6f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ab6f-123">-WhatIf</span></span>
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

### <span data-ttu-id="7ab6f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ab6f-124">CommonParameters</span></span>
<span data-ttu-id="7ab6f-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="7ab6f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ab6f-126">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="7ab6f-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ab6f-127">輸入</span><span class="sxs-lookup"><span data-stu-id="7ab6f-127">INPUTS</span></span>

### <span data-ttu-id="7ab6f-128">System.String</span><span class="sxs-lookup"><span data-stu-id="7ab6f-128">System.String</span></span>

### <span data-ttu-id="7ab6f-129">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="7ab6f-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="7ab6f-130">輸出</span><span class="sxs-lookup"><span data-stu-id="7ab6f-130">OUTPUTS</span></span>

### <span data-ttu-id="7ab6f-131">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7ab6f-131">System.Boolean</span></span>

## <span data-ttu-id="7ab6f-132">筆記</span><span class="sxs-lookup"><span data-stu-id="7ab6f-132">NOTES</span></span>

## <span data-ttu-id="7ab6f-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="7ab6f-133">RELATED LINKS</span></span>
