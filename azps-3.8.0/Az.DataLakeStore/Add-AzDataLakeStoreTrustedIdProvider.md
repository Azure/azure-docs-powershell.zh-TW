---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 5C788778-58A4-4798-AB66-1D3562BB9338
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/add-azdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: b6647ab3b729ab76d3cc02687bcd8dc342e788b4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93956462"
---
# <span data-ttu-id="92922-101">Add-AzDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="92922-101">Add-AzDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="92922-102">摘要</span><span class="sxs-lookup"><span data-stu-id="92922-102">SYNOPSIS</span></span>
<span data-ttu-id="92922-103">將信任的身分識別提供者新增至指定的 Data Lake Store 帳戶。</span><span class="sxs-lookup"><span data-stu-id="92922-103">Adds a trusted identity provider to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="92922-104">句法</span><span class="sxs-lookup"><span data-stu-id="92922-104">SYNTAX</span></span>

```
Add-AzDataLakeStoreTrustedIdProvider [-Account] <String> [-Name] <String> [-ProviderEndpoint] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="92922-105">說明</span><span class="sxs-lookup"><span data-stu-id="92922-105">DESCRIPTION</span></span>
<span data-ttu-id="92922-106">**AzDataLakeStoreTrustedIdProvider** Cmdlet 會將信任的身分識別提供者新增至指定的資料 Lake store 帳戶。</span><span class="sxs-lookup"><span data-stu-id="92922-106">The **Add-AzDataLakeStoreTrustedIdProvider** cmdlet adds a trusted identity provider to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="92922-107">示例</span><span class="sxs-lookup"><span data-stu-id="92922-107">EXAMPLES</span></span>

### <span data-ttu-id="92922-108">範例1：新增信任的身分識別提供者</span><span class="sxs-lookup"><span data-stu-id="92922-108">Example 1: Add a trusted identity provider</span></span>
```
PS C:\> Add-AzDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider -ProviderEndpoint "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"
```

<span data-ttu-id="92922-109">將提供者 "MyProvider" 新增至提供者端點 "" 的帳戶 "ContosoADL" https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150</span><span class="sxs-lookup"><span data-stu-id="92922-109">Adds the provider "MyProvider" to account "ContosoADL" with the provider endpoint "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"</span></span>

## <span data-ttu-id="92922-110">參數</span><span class="sxs-lookup"><span data-stu-id="92922-110">PARAMETERS</span></span>

### <span data-ttu-id="92922-111">-帳戶</span><span class="sxs-lookup"><span data-stu-id="92922-111">-Account</span></span>
<span data-ttu-id="92922-112">要新增指定信任身分識別提供者的 Data Lake Store 帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="92922-112">The name of the Data Lake Store account to add the specified trusted identity provider to.</span></span>

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

### <span data-ttu-id="92922-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92922-113">-DefaultProfile</span></span>
<span data-ttu-id="92922-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="92922-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="92922-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="92922-115">-Name</span></span>
<span data-ttu-id="92922-116">要新增之信任身分識別提供者的名稱</span><span class="sxs-lookup"><span data-stu-id="92922-116">The name of the trusted identity provider to add</span></span>

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

### <span data-ttu-id="92922-117">-ProviderEndpoint</span><span class="sxs-lookup"><span data-stu-id="92922-117">-ProviderEndpoint</span></span>
<span data-ttu-id="92922-118">有效的信任提供者端點，格式為：身分 https://sts.windows.net/\<provider 識別 \> "</span><span class="sxs-lookup"><span data-stu-id="92922-118">The valid trusted provider endpoint in the format: https://sts.windows.net/\<provider identity\>"</span></span>

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

### <span data-ttu-id="92922-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92922-119">-ResourceGroupName</span></span>
<span data-ttu-id="92922-120">要在其中新增受信任身分識別提供者之帳戶的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="92922-120">Name of resource group under which the account to add the trusted identity provider is.</span></span>

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

### <span data-ttu-id="92922-121">-確認</span><span class="sxs-lookup"><span data-stu-id="92922-121">-Confirm</span></span>
<span data-ttu-id="92922-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="92922-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92922-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92922-123">-WhatIf</span></span>
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

### <span data-ttu-id="92922-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92922-124">CommonParameters</span></span>
<span data-ttu-id="92922-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="92922-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92922-126">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="92922-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92922-127">輸入</span><span class="sxs-lookup"><span data-stu-id="92922-127">INPUTS</span></span>

### <span data-ttu-id="92922-128">System.object</span><span class="sxs-lookup"><span data-stu-id="92922-128">System.String</span></span>

## <span data-ttu-id="92922-129">輸出</span><span class="sxs-lookup"><span data-stu-id="92922-129">OUTPUTS</span></span>

### <span data-ttu-id="92922-130">DataLakeStoreTrustedIdProvider 中的 DataLakeStore。</span><span class="sxs-lookup"><span data-stu-id="92922-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="92922-131">筆記</span><span class="sxs-lookup"><span data-stu-id="92922-131">NOTES</span></span>

## <span data-ttu-id="92922-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="92922-132">RELATED LINKS</span></span>