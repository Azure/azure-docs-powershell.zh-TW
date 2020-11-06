---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 30C10687-F172-4663-8D4A-F0DDEA5C3741
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/remove-azurermdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: f281192e22cd8acdf85e389d82ef7146590be158
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93443860"
---
# <span data-ttu-id="976d2-101">Remove-AzureRmDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="976d2-101">Remove-AzureRmDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="976d2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="976d2-102">SYNOPSIS</span></span>
<span data-ttu-id="976d2-103">移除指定資料 Lake Store 中指定的信任身分識別提供者。</span><span class="sxs-lookup"><span data-stu-id="976d2-103">Removes the specified trusted identity provider in the specified Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="976d2-104">句法</span><span class="sxs-lookup"><span data-stu-id="976d2-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeStoreTrustedIdProvider [-Account] <String> [[-Name] <String>] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="976d2-105">說明</span><span class="sxs-lookup"><span data-stu-id="976d2-105">DESCRIPTION</span></span>
<span data-ttu-id="976d2-106">**AzureRmDataLakeStoreTrustedIdProvider** Cmdlet 會在指定的 Data Lake store 中移除指定的信任身分識別提供者。</span><span class="sxs-lookup"><span data-stu-id="976d2-106">The **Remove-AzureRmDataLakeStoreTrustedIdProvider** cmdlet removes the specified trusted identity provider in the specified Data Lake Store.</span></span>

## <span data-ttu-id="976d2-107">示例</span><span class="sxs-lookup"><span data-stu-id="976d2-107">EXAMPLES</span></span>

### <span data-ttu-id="976d2-108">範例1：移除信任的身分識別提供者。</span><span class="sxs-lookup"><span data-stu-id="976d2-108">Example 1: Remove a trusted identity provider.</span></span>
```
PS C:\> Remove-AzureRmDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider
```

<span data-ttu-id="976d2-109">從帳戶 "ContosoADL" 移除提供者 "MyProvider"</span><span class="sxs-lookup"><span data-stu-id="976d2-109">Removes the provider "MyProvider" from account "ContosoADL"</span></span>

## <span data-ttu-id="976d2-110">參數</span><span class="sxs-lookup"><span data-stu-id="976d2-110">PARAMETERS</span></span>

### <span data-ttu-id="976d2-111">-帳戶</span><span class="sxs-lookup"><span data-stu-id="976d2-111">-Account</span></span>
<span data-ttu-id="976d2-112">要從中移除信任身分識別提供者的 Data Lake Store 帳戶</span><span class="sxs-lookup"><span data-stu-id="976d2-112">The Data Lake Store account to remove the trusted identity provider from</span></span>

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

### <span data-ttu-id="976d2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="976d2-113">-DefaultProfile</span></span>
<span data-ttu-id="976d2-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="976d2-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="976d2-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="976d2-115">-Name</span></span>
<span data-ttu-id="976d2-116">信任身分識別提供者的名稱。</span><span class="sxs-lookup"><span data-stu-id="976d2-116">The name of the trusted identity provider.</span></span>

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

### <span data-ttu-id="976d2-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="976d2-117">-PassThru</span></span>
<span data-ttu-id="976d2-118">表示應傳回指示刪除操作結果的布林回應。</span><span class="sxs-lookup"><span data-stu-id="976d2-118">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="976d2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="976d2-119">-ResourceGroupName</span></span>
<span data-ttu-id="976d2-120">指定包含要從中移除信任身分識別提供者之帳戶的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="976d2-120">Specifies the name of the resource group that contains the account to remove the trusted identity provider from.</span></span>

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

### <span data-ttu-id="976d2-121">-確認</span><span class="sxs-lookup"><span data-stu-id="976d2-121">-Confirm</span></span>
<span data-ttu-id="976d2-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="976d2-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="976d2-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="976d2-123">-WhatIf</span></span>
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

### <span data-ttu-id="976d2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="976d2-124">CommonParameters</span></span>
<span data-ttu-id="976d2-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="976d2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="976d2-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="976d2-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="976d2-127">輸入</span><span class="sxs-lookup"><span data-stu-id="976d2-127">INPUTS</span></span>

### <span data-ttu-id="976d2-128">System.object</span><span class="sxs-lookup"><span data-stu-id="976d2-128">System.String</span></span>

### <span data-ttu-id="976d2-129">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="976d2-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="976d2-130">輸出</span><span class="sxs-lookup"><span data-stu-id="976d2-130">OUTPUTS</span></span>

### <span data-ttu-id="976d2-131">System.object</span><span class="sxs-lookup"><span data-stu-id="976d2-131">System.Boolean</span></span>

## <span data-ttu-id="976d2-132">筆記</span><span class="sxs-lookup"><span data-stu-id="976d2-132">NOTES</span></span>

## <span data-ttu-id="976d2-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="976d2-133">RELATED LINKS</span></span>
