---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 5C788778-58A4-4798-AB66-1D3562BB9338
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/add-azdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: 31ac134dc580fc23876a2fd4f9b75e60b23748e1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912877"
---
# <span data-ttu-id="b1c2f-101">Add-AzDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="b1c2f-101">Add-AzDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="b1c2f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b1c2f-102">SYNOPSIS</span></span>
<span data-ttu-id="b1c2f-103">將信任的身分識別提供者新增到指定的 Data Lake Store 帳戶。</span><span class="sxs-lookup"><span data-stu-id="b1c2f-103">Adds a trusted identity provider to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="b1c2f-104">語法</span><span class="sxs-lookup"><span data-stu-id="b1c2f-104">SYNTAX</span></span>

```
Add-AzDataLakeStoreTrustedIdProvider [-Account] <String> [-Name] <String> [-ProviderEndpoint] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b1c2f-105">描述</span><span class="sxs-lookup"><span data-stu-id="b1c2f-105">DESCRIPTION</span></span>
<span data-ttu-id="b1c2f-106">**Add-AzDataLakeStoreTrustedIdProvider Cmdlet** 會將信任的身分識別提供者新增到指定的 Data Lake Store 帳戶。</span><span class="sxs-lookup"><span data-stu-id="b1c2f-106">The **Add-AzDataLakeStoreTrustedIdProvider** cmdlet adds a trusted identity provider to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="b1c2f-107">例子</span><span class="sxs-lookup"><span data-stu-id="b1c2f-107">EXAMPLES</span></span>

### <span data-ttu-id="b1c2f-108">範例 1：新增信任的身分識別提供者</span><span class="sxs-lookup"><span data-stu-id="b1c2f-108">Example 1: Add a trusted identity provider</span></span>
```
PS C:\> Add-AzDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider -ProviderEndpoint "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"
```

<span data-ttu-id="b1c2f-109">將提供者 "MyProvider" 新增到帳戶 "ContosoADL" 與提供者端點 https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150 "</span><span class="sxs-lookup"><span data-stu-id="b1c2f-109">Adds the provider "MyProvider" to account "ContosoADL" with the provider endpoint "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"</span></span>

## <span data-ttu-id="b1c2f-110">參數</span><span class="sxs-lookup"><span data-stu-id="b1c2f-110">PARAMETERS</span></span>

### <span data-ttu-id="b1c2f-111">-帳戶</span><span class="sxs-lookup"><span data-stu-id="b1c2f-111">-Account</span></span>
<span data-ttu-id="b1c2f-112">要新增指定信任的身分識別提供者的 Data Lake Store 帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="b1c2f-112">The name of the Data Lake Store account to add the specified trusted identity provider to.</span></span>

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

### <span data-ttu-id="b1c2f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1c2f-113">-DefaultProfile</span></span>
<span data-ttu-id="b1c2f-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="b1c2f-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b1c2f-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="b1c2f-115">-Name</span></span>
<span data-ttu-id="b1c2f-116">要新增之信任的身分識別提供者名稱</span><span class="sxs-lookup"><span data-stu-id="b1c2f-116">The name of the trusted identity provider to add</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1c2f-117">-ProviderEndpoint</span><span class="sxs-lookup"><span data-stu-id="b1c2f-117">-ProviderEndpoint</span></span>
<span data-ttu-id="b1c2f-118">格式為「」的有效信任提供者 https://sts.windows.net/ 端點： \<provider identity\></span><span class="sxs-lookup"><span data-stu-id="b1c2f-118">The valid trusted provider endpoint in the format: https://sts.windows.net/\<provider identity\>"</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1c2f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1c2f-119">-ResourceGroupName</span></span>
<span data-ttu-id="b1c2f-120">要新增信任身分識別提供者之帳戶的資源組名。</span><span class="sxs-lookup"><span data-stu-id="b1c2f-120">Name of resource group under which the account to add the trusted identity provider is.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1c2f-121">-確認</span><span class="sxs-lookup"><span data-stu-id="b1c2f-121">-Confirm</span></span>
<span data-ttu-id="b1c2f-122">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="b1c2f-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1c2f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1c2f-123">-WhatIf</span></span>
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

### <span data-ttu-id="b1c2f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1c2f-124">CommonParameters</span></span>
<span data-ttu-id="b1c2f-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b1c2f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1c2f-126">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="b1c2f-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1c2f-127">輸入</span><span class="sxs-lookup"><span data-stu-id="b1c2f-127">INPUTS</span></span>

### <span data-ttu-id="b1c2f-128">System.String</span><span class="sxs-lookup"><span data-stu-id="b1c2f-128">System.String</span></span>

## <span data-ttu-id="b1c2f-129">輸出</span><span class="sxs-lookup"><span data-stu-id="b1c2f-129">OUTPUTS</span></span>

### <span data-ttu-id="b1c2f-130">Microsoft.Azure.Commands.DataLakeStore.models.DataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="b1c2f-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="b1c2f-131">筆記</span><span class="sxs-lookup"><span data-stu-id="b1c2f-131">NOTES</span></span>

## <span data-ttu-id="b1c2f-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="b1c2f-132">RELATED LINKS</span></span>
