---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: BDEF8BAA-0C64-465D-9ED4-6FEFC1E850CC
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: c4de7a926e4095ad8bb45a25647305617988330d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94284978"
---
# <span data-ttu-id="1463f-101">Set-AzDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="1463f-101">Set-AzDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="1463f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1463f-102">SYNOPSIS</span></span>
<span data-ttu-id="1463f-103">在指定的 Data Lake Store 中修改指定的信任身分識別提供者。</span><span class="sxs-lookup"><span data-stu-id="1463f-103">Modifies the specified trusted identity provider in the specified Data Lake Store.</span></span>

## <span data-ttu-id="1463f-104">句法</span><span class="sxs-lookup"><span data-stu-id="1463f-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreTrustedIdProvider [-Account] <String> [-Name] <String> [-ProviderEndpoint] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1463f-105">說明</span><span class="sxs-lookup"><span data-stu-id="1463f-105">DESCRIPTION</span></span>
<span data-ttu-id="1463f-106">**AzDataLakeStoreTrustedIdProvider** Cmdlet 會修改指定資料 Lake store 中指定的信任身分識別提供者。</span><span class="sxs-lookup"><span data-stu-id="1463f-106">The **Set-AzDataLakeStoreTrustedIdProvider** cmdlet modifies the specified trusted identity provider in the specified Data Lake Store.</span></span>

## <span data-ttu-id="1463f-107">示例</span><span class="sxs-lookup"><span data-stu-id="1463f-107">EXAMPLES</span></span>

### <span data-ttu-id="1463f-108">範例1：更新信任的身分識別提供者端點</span><span class="sxs-lookup"><span data-stu-id="1463f-108">Example 1: Update a Trusted Identity Provider Endpoint</span></span>
```
PS C:\> Set-AzDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider -ProviderEndpoint "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"
```

<span data-ttu-id="1463f-109">這會將帳戶 "ContosoADL" 中的防火牆規則 "MyProvider" 的提供者端點更新為 " https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150 "</span><span class="sxs-lookup"><span data-stu-id="1463f-109">This updates the provider endpoint for firewall rule "MyProvider" in account "ContosoADL" to "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"</span></span>

## <span data-ttu-id="1463f-110">參數</span><span class="sxs-lookup"><span data-stu-id="1463f-110">PARAMETERS</span></span>

### <span data-ttu-id="1463f-111">-帳戶</span><span class="sxs-lookup"><span data-stu-id="1463f-111">-Account</span></span>
<span data-ttu-id="1463f-112">要新增信任身分識別提供者的 Data Lake Store 帳戶</span><span class="sxs-lookup"><span data-stu-id="1463f-112">The Data Lake Store account to add the trusted identity provider to</span></span>

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

### <span data-ttu-id="1463f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1463f-113">-DefaultProfile</span></span>
<span data-ttu-id="1463f-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="1463f-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1463f-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="1463f-115">-Name</span></span>
<span data-ttu-id="1463f-116">信任身分識別提供者的名稱。</span><span class="sxs-lookup"><span data-stu-id="1463f-116">The name of the trusted identity provider.</span></span>

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

### <span data-ttu-id="1463f-117">-ProviderEndpoint</span><span class="sxs-lookup"><span data-stu-id="1463f-117">-ProviderEndpoint</span></span>
<span data-ttu-id="1463f-118">有效信任提供者端點的格式為： https://sts.windows.net/\<provider identity\></span><span class="sxs-lookup"><span data-stu-id="1463f-118">The valid trusted provider endpoint in the format: https://sts.windows.net/\<provider identity\></span></span>

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

### <span data-ttu-id="1463f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1463f-119">-ResourceGroupName</span></span>
<span data-ttu-id="1463f-120">指定包含要為其更新信任身分識別提供者之帳戶的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1463f-120">Specifies the name of the resource group that contains the account to update the trusted identity provider for.</span></span>

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

### <span data-ttu-id="1463f-121">-確認</span><span class="sxs-lookup"><span data-stu-id="1463f-121">-Confirm</span></span>
<span data-ttu-id="1463f-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1463f-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1463f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1463f-123">-WhatIf</span></span>
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

### <span data-ttu-id="1463f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1463f-124">CommonParameters</span></span>
<span data-ttu-id="1463f-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1463f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1463f-126">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1463f-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1463f-127">輸入</span><span class="sxs-lookup"><span data-stu-id="1463f-127">INPUTS</span></span>

### <span data-ttu-id="1463f-128">System.object</span><span class="sxs-lookup"><span data-stu-id="1463f-128">System.String</span></span>

## <span data-ttu-id="1463f-129">輸出</span><span class="sxs-lookup"><span data-stu-id="1463f-129">OUTPUTS</span></span>

### <span data-ttu-id="1463f-130">DataLakeStoreTrustedIdProvider 中的 DataLakeStore。</span><span class="sxs-lookup"><span data-stu-id="1463f-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="1463f-131">筆記</span><span class="sxs-lookup"><span data-stu-id="1463f-131">NOTES</span></span>

## <span data-ttu-id="1463f-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="1463f-132">RELATED LINKS</span></span>
