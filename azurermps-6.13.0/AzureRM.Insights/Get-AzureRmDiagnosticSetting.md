---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 60B497F6-98A2-4C60-B142-FF5CD123362D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermdiagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmDiagnosticSetting.md
ms.openlocfilehash: 2b70fd58bd0b51e03079b1c24665b67ac3ad3a2d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449132"
---
# <span data-ttu-id="db4f4-101">Get-AzureRmDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="db4f4-101">Get-AzureRmDiagnosticSetting</span></span>

## <span data-ttu-id="db4f4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="db4f4-102">SYNOPSIS</span></span>
<span data-ttu-id="db4f4-103">取得已記錄的類別和時間 grains。</span><span class="sxs-lookup"><span data-stu-id="db4f4-103">Gets the logged categories and time grains.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="db4f4-104">句法</span><span class="sxs-lookup"><span data-stu-id="db4f4-104">SYNTAX</span></span>

```
Get-AzureRmDiagnosticSetting [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="db4f4-105">說明</span><span class="sxs-lookup"><span data-stu-id="db4f4-105">DESCRIPTION</span></span>
<span data-ttu-id="db4f4-106">**AzureRmDiagnosticSetting** Cmdlet 會取得記錄給資源的類別和時間 grains。</span><span class="sxs-lookup"><span data-stu-id="db4f4-106">The **Get-AzureRmDiagnosticSetting** cmdlet gets the categories and time grains that are logged for a resource.</span></span>
<span data-ttu-id="db4f4-107">時間細微性是度量的匯總間隔。</span><span class="sxs-lookup"><span data-stu-id="db4f4-107">A time grain is the aggregation interval of a metric.</span></span>

## <span data-ttu-id="db4f4-108">示例</span><span class="sxs-lookup"><span data-stu-id="db4f4-108">EXAMPLES</span></span>

### <span data-ttu-id="db4f4-109">範例1：取得記錄類別與時間 grains 的狀態</span><span class="sxs-lookup"><span data-stu-id="db4f4-109">Example 1: Get the status of the logging categories and time grains</span></span>
```
PS C:\>Get-AzureRmDiagnosticSetting -ResourceId "/subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.keyvault/KeyVaults/ContosoKeyVault"
StorageAccountId   : /subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.storage/accounts/ContosoStorageAccount
StorageAccountName : ContosoStorageAccount001
Metrics

Logs
Enabled  : True
Category : AuditEvent
```

<span data-ttu-id="db4f4-110">這個命令會取得針對 Azure 金鑰保存庫記錄的類別和時間 grains，其中包含/subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.keyvault/KeyVaults/ContosoKeyVault. 的 *ResourceId*</span><span class="sxs-lookup"><span data-stu-id="db4f4-110">This command gets the categories and time grains that are logged for an Azure Key Vault with a *ResourceId* of /subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.keyvault/KeyVaults/ContosoKeyVault.</span></span>

## <span data-ttu-id="db4f4-111">參數</span><span class="sxs-lookup"><span data-stu-id="db4f4-111">PARAMETERS</span></span>

### <span data-ttu-id="db4f4-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db4f4-112">-DefaultProfile</span></span>
<span data-ttu-id="db4f4-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="db4f4-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="db4f4-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="db4f4-114">-Name</span></span>
<span data-ttu-id="db4f4-115">診斷設定的名稱。</span><span class="sxs-lookup"><span data-stu-id="db4f4-115">The name of the diagnostic setting.</span></span> <span data-ttu-id="db4f4-116">如果未指定呼叫預設為「服務」，就像它在前一個 API 中一樣。</span><span class="sxs-lookup"><span data-stu-id="db4f4-116">If not given the call default to "service" as it was in the previous API.</span></span>

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

### <span data-ttu-id="db4f4-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="db4f4-117">-ResourceId</span></span>
<span data-ttu-id="db4f4-118">指定資源的識別碼。</span><span class="sxs-lookup"><span data-stu-id="db4f4-118">Specifies the ID of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db4f4-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db4f4-119">CommonParameters</span></span>
<span data-ttu-id="db4f4-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="db4f4-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db4f4-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="db4f4-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db4f4-122">輸入</span><span class="sxs-lookup"><span data-stu-id="db4f4-122">INPUTS</span></span>

### <span data-ttu-id="db4f4-123">System.object</span><span class="sxs-lookup"><span data-stu-id="db4f4-123">System.String</span></span>

## <span data-ttu-id="db4f4-124">輸出</span><span class="sxs-lookup"><span data-stu-id="db4f4-124">OUTPUTS</span></span>

### <span data-ttu-id="db4f4-125">PSServiceDiagnosticSettings 中的 OutputClasses。</span><span class="sxs-lookup"><span data-stu-id="db4f4-125">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

## <span data-ttu-id="db4f4-126">筆記</span><span class="sxs-lookup"><span data-stu-id="db4f4-126">NOTES</span></span>

## <span data-ttu-id="db4f4-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="db4f4-127">RELATED LINKS</span></span>

<span data-ttu-id="db4f4-128">[Set-AzureRmDiagnosticSetting](./Set-AzureRmDiagnosticSetting.md) 
[移除-AzureRmDiagnosticSetting](./Remove-AzureRmDiagnosticSetting.md)</span><span class="sxs-lookup"><span data-stu-id="db4f4-128">[Set-AzureRmDiagnosticSetting](./Set-AzureRmDiagnosticSetting.md)
[Remove-AzureRmDiagnosticSetting](./Remove-AzureRmDiagnosticSetting.md)</span></span>
