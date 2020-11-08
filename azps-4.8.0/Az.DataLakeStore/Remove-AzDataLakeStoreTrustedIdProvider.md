---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 30C10687-F172-4663-8D4A-F0DDEA5C3741
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/remove-azdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: 3e16db29f6560778dff5c86ac222d06fd41a5807
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94128456"
---
# <span data-ttu-id="00176-101">Remove-AzDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="00176-101">Remove-AzDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="00176-102">摘要</span><span class="sxs-lookup"><span data-stu-id="00176-102">SYNOPSIS</span></span>
<span data-ttu-id="00176-103">移除指定資料 Lake Store 中指定的信任身分識別提供者。</span><span class="sxs-lookup"><span data-stu-id="00176-103">Removes the specified trusted identity provider in the specified Data Lake Store.</span></span>

## <span data-ttu-id="00176-104">句法</span><span class="sxs-lookup"><span data-stu-id="00176-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreTrustedIdProvider [-Account] <String> [[-Name] <String>] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="00176-105">說明</span><span class="sxs-lookup"><span data-stu-id="00176-105">DESCRIPTION</span></span>
<span data-ttu-id="00176-106">**AzDataLakeStoreTrustedIdProvider** Cmdlet 會在指定的 Data Lake store 中移除指定的信任身分識別提供者。</span><span class="sxs-lookup"><span data-stu-id="00176-106">The **Remove-AzDataLakeStoreTrustedIdProvider** cmdlet removes the specified trusted identity provider in the specified Data Lake Store.</span></span>

## <span data-ttu-id="00176-107">示例</span><span class="sxs-lookup"><span data-stu-id="00176-107">EXAMPLES</span></span>

### <span data-ttu-id="00176-108">範例1：移除信任的身分識別提供者。</span><span class="sxs-lookup"><span data-stu-id="00176-108">Example 1: Remove a trusted identity provider.</span></span>
```
PS C:\> Remove-AzDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider
```

<span data-ttu-id="00176-109">從帳戶 "ContosoADL" 移除提供者 "MyProvider"</span><span class="sxs-lookup"><span data-stu-id="00176-109">Removes the provider "MyProvider" from account "ContosoADL"</span></span>

## <span data-ttu-id="00176-110">參數</span><span class="sxs-lookup"><span data-stu-id="00176-110">PARAMETERS</span></span>

### <span data-ttu-id="00176-111">-帳戶</span><span class="sxs-lookup"><span data-stu-id="00176-111">-Account</span></span>
<span data-ttu-id="00176-112">要從中移除信任身分識別提供者的 Data Lake Store 帳戶</span><span class="sxs-lookup"><span data-stu-id="00176-112">The Data Lake Store account to remove the trusted identity provider from</span></span>

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

### <span data-ttu-id="00176-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00176-113">-DefaultProfile</span></span>
<span data-ttu-id="00176-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="00176-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="00176-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="00176-115">-Name</span></span>
<span data-ttu-id="00176-116">信任身分識別提供者的名稱。</span><span class="sxs-lookup"><span data-stu-id="00176-116">The name of the trusted identity provider.</span></span>

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

### <span data-ttu-id="00176-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="00176-117">-PassThru</span></span>
<span data-ttu-id="00176-118">表示應傳回指示刪除操作結果的布林回應。</span><span class="sxs-lookup"><span data-stu-id="00176-118">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="00176-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00176-119">-ResourceGroupName</span></span>
<span data-ttu-id="00176-120">指定包含要從中移除信任身分識別提供者之帳戶的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="00176-120">Specifies the name of the resource group that contains the account to remove the trusted identity provider from.</span></span>

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

### <span data-ttu-id="00176-121">-確認</span><span class="sxs-lookup"><span data-stu-id="00176-121">-Confirm</span></span>
<span data-ttu-id="00176-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="00176-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00176-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00176-123">-WhatIf</span></span>
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

### <span data-ttu-id="00176-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00176-124">CommonParameters</span></span>
<span data-ttu-id="00176-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="00176-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00176-126">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="00176-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00176-127">輸入</span><span class="sxs-lookup"><span data-stu-id="00176-127">INPUTS</span></span>

### <span data-ttu-id="00176-128">System.object</span><span class="sxs-lookup"><span data-stu-id="00176-128">System.String</span></span>

### <span data-ttu-id="00176-129">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="00176-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="00176-130">輸出</span><span class="sxs-lookup"><span data-stu-id="00176-130">OUTPUTS</span></span>

### <span data-ttu-id="00176-131">System.object</span><span class="sxs-lookup"><span data-stu-id="00176-131">System.Boolean</span></span>

## <span data-ttu-id="00176-132">筆記</span><span class="sxs-lookup"><span data-stu-id="00176-132">NOTES</span></span>

## <span data-ttu-id="00176-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="00176-133">RELATED LINKS</span></span>