---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 60B497F6-98A2-4C60-B142-FF5CD123362D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmDiagnosticSetting.md
ms.openlocfilehash: 236ce405c222ba3b7746ba1affca8f288045f8a1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625179"
---
# <span data-ttu-id="66a98-101">Get-AzureRmDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="66a98-101">Get-AzureRmDiagnosticSetting</span></span>

## <span data-ttu-id="66a98-102">摘要</span><span class="sxs-lookup"><span data-stu-id="66a98-102">SYNOPSIS</span></span>
<span data-ttu-id="66a98-103">取得已記錄的類別和時間 grains。</span><span class="sxs-lookup"><span data-stu-id="66a98-103">Gets the logged categories and time grains.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="66a98-104">句法</span><span class="sxs-lookup"><span data-stu-id="66a98-104">SYNTAX</span></span>

```
Get-AzureRmDiagnosticSetting [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="66a98-105">說明</span><span class="sxs-lookup"><span data-stu-id="66a98-105">DESCRIPTION</span></span>
<span data-ttu-id="66a98-106">**AzureRmDiagnosticSetting** Cmdlet 會取得記錄給資源的類別和時間 grains。</span><span class="sxs-lookup"><span data-stu-id="66a98-106">The **Get-AzureRmDiagnosticSetting** cmdlet gets the categories and time grains that are logged for a resource.</span></span>

<span data-ttu-id="66a98-107">時間細微性是度量的匯總間隔。</span><span class="sxs-lookup"><span data-stu-id="66a98-107">A time grain is the aggregation interval of a metric.</span></span>

## <span data-ttu-id="66a98-108">示例</span><span class="sxs-lookup"><span data-stu-id="66a98-108">EXAMPLES</span></span>

### <span data-ttu-id="66a98-109">範例1：取得記錄類別與時間 grains 的狀態</span><span class="sxs-lookup"><span data-stu-id="66a98-109">Example 1: Get the status of the logging categories and time grains</span></span>
```
PS C:\>Get-AzureRmDiagnosticSetting -ResourceId "/subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.keyvault/KeyVaults/ContosoKeyVault"
StorageAccountId   : /subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.storage/accounts/ContosoStorageAccount
StorageAccountName : ContosoStorageAccount001
Metrics

Logs
Enabled  : True
Category : AuditEvent
```

<span data-ttu-id="66a98-110">這個命令會取得針對 Azure 金鑰保存庫記錄的類別和時間 grains，其中包含/subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.keyvault/KeyVaults/ContosoKeyVault. 的 *ResourceId*</span><span class="sxs-lookup"><span data-stu-id="66a98-110">This command gets the categories and time grains that are logged for an Azure Key Vault with a *ResourceId* of /subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.keyvault/KeyVaults/ContosoKeyVault.</span></span>

## <span data-ttu-id="66a98-111">參數</span><span class="sxs-lookup"><span data-stu-id="66a98-111">PARAMETERS</span></span>

### <span data-ttu-id="66a98-112">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="66a98-112">-ResourceId</span></span>
<span data-ttu-id="66a98-113">指定資源的識別碼。</span><span class="sxs-lookup"><span data-stu-id="66a98-113">Specifies the ID of the resource.</span></span>

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

### <span data-ttu-id="66a98-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66a98-114">-DefaultProfile</span></span>
<span data-ttu-id="66a98-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="66a98-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="66a98-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66a98-116">CommonParameters</span></span>
<span data-ttu-id="66a98-117">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="66a98-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66a98-118">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="66a98-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66a98-119">輸入</span><span class="sxs-lookup"><span data-stu-id="66a98-119">INPUTS</span></span>

## <span data-ttu-id="66a98-120">輸出</span><span class="sxs-lookup"><span data-stu-id="66a98-120">OUTPUTS</span></span>

### <span data-ttu-id="66a98-121">PSServiceDiagnosticSettings 中的 OutputClasses。</span><span class="sxs-lookup"><span data-stu-id="66a98-121">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

## <span data-ttu-id="66a98-122">筆記</span><span class="sxs-lookup"><span data-stu-id="66a98-122">NOTES</span></span>

## <span data-ttu-id="66a98-123">相關連結</span><span class="sxs-lookup"><span data-stu-id="66a98-123">RELATED LINKS</span></span>

[<span data-ttu-id="66a98-124">AzureRmDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="66a98-124">Get-AzureRmDiagnosticSetting</span></span>](./Get-AzureRmDiagnosticSetting.md)


