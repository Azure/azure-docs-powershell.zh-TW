---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: BDEF8BAA-0C64-465D-9ED4-6FEFC1E850CC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/set-azurermdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: 29f9bbab5d3f7590d53bc405d80ea9e5c484fd5e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449903"
---
# <span data-ttu-id="12ef3-101">Set-AzureRmDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="12ef3-101">Set-AzureRmDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="12ef3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="12ef3-102">SYNOPSIS</span></span>
<span data-ttu-id="12ef3-103">在指定的 Data Lake Store 中修改指定的信任身分識別提供者。</span><span class="sxs-lookup"><span data-stu-id="12ef3-103">Modifies the specified trusted identity provider in the specified Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="12ef3-104">句法</span><span class="sxs-lookup"><span data-stu-id="12ef3-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeStoreTrustedIdProvider [-Account] <String> [-Name] <String> [-ProviderEndpoint] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="12ef3-105">說明</span><span class="sxs-lookup"><span data-stu-id="12ef3-105">DESCRIPTION</span></span>
<span data-ttu-id="12ef3-106">**AzureRmDataLakeStoreTrustedIdProvider** Cmdlet 會修改指定資料 Lake store 中指定的信任身分識別提供者。</span><span class="sxs-lookup"><span data-stu-id="12ef3-106">The **Set-AzureRmDataLakeStoreTrustedIdProvider** cmdlet modifies the specified trusted identity provider in the specified Data Lake Store.</span></span>

## <span data-ttu-id="12ef3-107">示例</span><span class="sxs-lookup"><span data-stu-id="12ef3-107">EXAMPLES</span></span>

### <span data-ttu-id="12ef3-108">範例1：更新信任的身分識別提供者端點</span><span class="sxs-lookup"><span data-stu-id="12ef3-108">Example 1: Update a Trusted Identity Provider Endpoint</span></span>
```
PS C:\> Set-AzureRmDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider -ProviderEndpoint "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"
```

<span data-ttu-id="12ef3-109">這會將帳戶 "ContosoADL" 中的防火牆規則 "MyProvider" 的提供者 endpoing 更新為 " https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150 "</span><span class="sxs-lookup"><span data-stu-id="12ef3-109">This updates the provider endpoing for firewall rule "MyProvider" in account "ContosoADL" to "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"</span></span>

## <span data-ttu-id="12ef3-110">參數</span><span class="sxs-lookup"><span data-stu-id="12ef3-110">PARAMETERS</span></span>

### <span data-ttu-id="12ef3-111">-帳戶</span><span class="sxs-lookup"><span data-stu-id="12ef3-111">-Account</span></span>
<span data-ttu-id="12ef3-112">要新增信任身分識別提供者的 Data Lake Store 帳戶</span><span class="sxs-lookup"><span data-stu-id="12ef3-112">The Data Lake Store account to add the trusted identity provider to</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12ef3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12ef3-113">-DefaultProfile</span></span>
<span data-ttu-id="12ef3-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="12ef3-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12ef3-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="12ef3-115">-Name</span></span>
<span data-ttu-id="12ef3-116">信任身分識別提供者的名稱。</span><span class="sxs-lookup"><span data-stu-id="12ef3-116">The name of the trusted identity provider.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12ef3-117">-ProviderEndpoint</span><span class="sxs-lookup"><span data-stu-id="12ef3-117">-ProviderEndpoint</span></span>
<span data-ttu-id="12ef3-118">有效信任提供者端點的格式為： https://sts.windows.net/\<provider identity\></span><span class="sxs-lookup"><span data-stu-id="12ef3-118">The valid trusted provider endpoint in the format: https://sts.windows.net/\<provider identity\></span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12ef3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12ef3-119">-ResourceGroupName</span></span>
<span data-ttu-id="12ef3-120">指定包含要為其更新信任身分識別提供者之帳戶的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="12ef3-120">Specifies the name of the resource group that contains the account to update the trusted identity provider for.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12ef3-121">-確認</span><span class="sxs-lookup"><span data-stu-id="12ef3-121">-Confirm</span></span>
<span data-ttu-id="12ef3-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="12ef3-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12ef3-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12ef3-123">-WhatIf</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12ef3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12ef3-124">CommonParameters</span></span>
<span data-ttu-id="12ef3-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="12ef3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12ef3-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="12ef3-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12ef3-127">輸入</span><span class="sxs-lookup"><span data-stu-id="12ef3-127">INPUTS</span></span>

### <span data-ttu-id="12ef3-128">所有</span><span class="sxs-lookup"><span data-stu-id="12ef3-128">None</span></span>
<span data-ttu-id="12ef3-129">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="12ef3-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="12ef3-130">輸出</span><span class="sxs-lookup"><span data-stu-id="12ef3-130">OUTPUTS</span></span>

### <span data-ttu-id="12ef3-131">DataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="12ef3-131">DataLakeStoreTrustedIdProvider</span></span>
<span data-ttu-id="12ef3-132">已更新的信任身分識別提供者。</span><span class="sxs-lookup"><span data-stu-id="12ef3-132">The updated trusted identity provider.</span></span>

## <span data-ttu-id="12ef3-133">筆記</span><span class="sxs-lookup"><span data-stu-id="12ef3-133">NOTES</span></span>

## <span data-ttu-id="12ef3-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="12ef3-134">RELATED LINKS</span></span>

