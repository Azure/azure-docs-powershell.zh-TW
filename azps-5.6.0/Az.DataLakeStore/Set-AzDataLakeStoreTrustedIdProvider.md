---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: BDEF8BAA-0C64-465D-9ED4-6FEFC1E850CC
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/set-azdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: 7efe0e21b6b433160eab36856d3419dc918cbfc4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913221"
---
# <span data-ttu-id="18056-101">Set-AzDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="18056-101">Set-AzDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="18056-102">簡介</span><span class="sxs-lookup"><span data-stu-id="18056-102">SYNOPSIS</span></span>
<span data-ttu-id="18056-103">修改指定 Data Lake Store 中指定的信任身分識別提供者。</span><span class="sxs-lookup"><span data-stu-id="18056-103">Modifies the specified trusted identity provider in the specified Data Lake Store.</span></span>

## <span data-ttu-id="18056-104">語法</span><span class="sxs-lookup"><span data-stu-id="18056-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreTrustedIdProvider [-Account] <String> [-Name] <String> [-ProviderEndpoint] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="18056-105">描述</span><span class="sxs-lookup"><span data-stu-id="18056-105">DESCRIPTION</span></span>
<span data-ttu-id="18056-106">**Set-AzDataLakeStoreTrustedIdProvider Cmdlet** 會修改指定 Data Lake Store 中指定的信任身分識別提供者。</span><span class="sxs-lookup"><span data-stu-id="18056-106">The **Set-AzDataLakeStoreTrustedIdProvider** cmdlet modifies the specified trusted identity provider in the specified Data Lake Store.</span></span>

## <span data-ttu-id="18056-107">例子</span><span class="sxs-lookup"><span data-stu-id="18056-107">EXAMPLES</span></span>

### <span data-ttu-id="18056-108">範例 1：更新信任的身分識別提供者端點</span><span class="sxs-lookup"><span data-stu-id="18056-108">Example 1: Update a Trusted Identity Provider Endpoint</span></span>
```
PS C:\> Set-AzDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider -ProviderEndpoint "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"
```

<span data-ttu-id="18056-109">這會將帳戶 "ContosoADL" 中防火牆規則 "MyProvider" 的提供者端點更新為 https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150 "</span><span class="sxs-lookup"><span data-stu-id="18056-109">This updates the provider endpoint for firewall rule "MyProvider" in account "ContosoADL" to "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"</span></span>

## <span data-ttu-id="18056-110">參數</span><span class="sxs-lookup"><span data-stu-id="18056-110">PARAMETERS</span></span>

### <span data-ttu-id="18056-111">-帳戶</span><span class="sxs-lookup"><span data-stu-id="18056-111">-Account</span></span>
<span data-ttu-id="18056-112">資料湖市管理帳戶，將信任的身分識別提供者新增到</span><span class="sxs-lookup"><span data-stu-id="18056-112">The Data Lake Store account to add the trusted identity provider to</span></span>

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

### <span data-ttu-id="18056-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18056-113">-DefaultProfile</span></span>
<span data-ttu-id="18056-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="18056-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="18056-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="18056-115">-Name</span></span>
<span data-ttu-id="18056-116">信任的身分識別提供者的名稱。</span><span class="sxs-lookup"><span data-stu-id="18056-116">The name of the trusted identity provider.</span></span>

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

### <span data-ttu-id="18056-117">-ProviderEndpoint</span><span class="sxs-lookup"><span data-stu-id="18056-117">-ProviderEndpoint</span></span>
<span data-ttu-id="18056-118">格式為有效信任的提供者端點： https://sts.windows.net/\<provider identity\></span><span class="sxs-lookup"><span data-stu-id="18056-118">The valid trusted provider endpoint in the format: https://sts.windows.net/\<provider identity\></span></span>

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

### <span data-ttu-id="18056-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18056-119">-ResourceGroupName</span></span>
<span data-ttu-id="18056-120">指定包含帳戶的資源組名，以更新信任的身分識別提供者。</span><span class="sxs-lookup"><span data-stu-id="18056-120">Specifies the name of the resource group that contains the account to update the trusted identity provider for.</span></span>

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

### <span data-ttu-id="18056-121">-確認</span><span class="sxs-lookup"><span data-stu-id="18056-121">-Confirm</span></span>
<span data-ttu-id="18056-122">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="18056-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18056-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18056-123">-WhatIf</span></span>
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

### <span data-ttu-id="18056-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18056-124">CommonParameters</span></span>
<span data-ttu-id="18056-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="18056-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18056-126">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="18056-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18056-127">輸入</span><span class="sxs-lookup"><span data-stu-id="18056-127">INPUTS</span></span>

### <span data-ttu-id="18056-128">System.String</span><span class="sxs-lookup"><span data-stu-id="18056-128">System.String</span></span>

## <span data-ttu-id="18056-129">輸出</span><span class="sxs-lookup"><span data-stu-id="18056-129">OUTPUTS</span></span>

### <span data-ttu-id="18056-130">Microsoft.Azure.Commands.DataLakeStore.models.DataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="18056-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="18056-131">筆記</span><span class="sxs-lookup"><span data-stu-id="18056-131">NOTES</span></span>

## <span data-ttu-id="18056-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="18056-132">RELATED LINKS</span></span>
