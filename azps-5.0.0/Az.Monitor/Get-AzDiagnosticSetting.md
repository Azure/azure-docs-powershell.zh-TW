---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 60B497F6-98A2-4C60-B142-FF5CD123362D
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azdiagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDiagnosticSetting.md
ms.openlocfilehash: d1a6859638bfbcb69e479f4bc18a6a36c8aa68fe
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94140046"
---
# <span data-ttu-id="d4a11-101">Get-AzDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="d4a11-101">Get-AzDiagnosticSetting</span></span>

## <span data-ttu-id="d4a11-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d4a11-102">SYNOPSIS</span></span>
<span data-ttu-id="d4a11-103">取得已記錄的類別和時間 grains。</span><span class="sxs-lookup"><span data-stu-id="d4a11-103">Gets the logged categories and time grains.</span></span>

## <span data-ttu-id="d4a11-104">句法</span><span class="sxs-lookup"><span data-stu-id="d4a11-104">SYNTAX</span></span>

```
Get-AzDiagnosticSetting [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d4a11-105">說明</span><span class="sxs-lookup"><span data-stu-id="d4a11-105">DESCRIPTION</span></span>
<span data-ttu-id="d4a11-106">**AzDiagnosticSetting** Cmdlet 會取得記錄給資源的類別和時間 grains。</span><span class="sxs-lookup"><span data-stu-id="d4a11-106">The **Get-AzDiagnosticSetting** cmdlet gets the categories and time grains that are logged for a resource.</span></span>
<span data-ttu-id="d4a11-107">時間細微性是度量的匯總間隔。</span><span class="sxs-lookup"><span data-stu-id="d4a11-107">A time grain is the aggregation interval of a metric.</span></span>

## <span data-ttu-id="d4a11-108">示例</span><span class="sxs-lookup"><span data-stu-id="d4a11-108">EXAMPLES</span></span>

### <span data-ttu-id="d4a11-109">範例1：取得記錄類別與時間 grains 的狀態</span><span class="sxs-lookup"><span data-stu-id="d4a11-109">Example 1: Get the status of the logging categories and time grains</span></span>
```
PS C:\>Get-AzDiagnosticSetting -ResourceId "/subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.keyvault/KeyVaults/ContosoKeyVault"
StorageAccountId   : /subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.storage/accounts/ContosoStorageAccount
StorageAccountName : ContosoStorageAccount001
Metrics

Logs
Enabled  : True
Category : AuditEvent
```

<span data-ttu-id="d4a11-110">這個命令會取得針對 Azure 金鑰保存庫記錄的類別和時間 grains，其中包含/subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.keyvault/KeyVaults/ContosoKeyVault. 的 *ResourceId*</span><span class="sxs-lookup"><span data-stu-id="d4a11-110">This command gets the categories and time grains that are logged for an Azure Key Vault with a *ResourceId* of /subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.keyvault/KeyVaults/ContosoKeyVault.</span></span>

## <span data-ttu-id="d4a11-111">參數</span><span class="sxs-lookup"><span data-stu-id="d4a11-111">PARAMETERS</span></span>

### <span data-ttu-id="d4a11-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4a11-112">-DefaultProfile</span></span>
<span data-ttu-id="d4a11-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="d4a11-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d4a11-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="d4a11-114">-Name</span></span>
<span data-ttu-id="d4a11-115">診斷設定的名稱。</span><span class="sxs-lookup"><span data-stu-id="d4a11-115">The name of the diagnostic setting.</span></span> <span data-ttu-id="d4a11-116">如果未指定呼叫預設為「服務」，就像它在前一個 API 中一樣。</span><span class="sxs-lookup"><span data-stu-id="d4a11-116">If not given the call default to "service" as it was in the previous API.</span></span>

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

### <span data-ttu-id="d4a11-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d4a11-117">-ResourceId</span></span>
<span data-ttu-id="d4a11-118">指定資源的識別碼。</span><span class="sxs-lookup"><span data-stu-id="d4a11-118">Specifies the ID of the resource.</span></span>

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

### <span data-ttu-id="d4a11-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4a11-119">CommonParameters</span></span>
<span data-ttu-id="d4a11-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d4a11-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4a11-121">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="d4a11-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4a11-122">輸入</span><span class="sxs-lookup"><span data-stu-id="d4a11-122">INPUTS</span></span>

### <span data-ttu-id="d4a11-123">System.object</span><span class="sxs-lookup"><span data-stu-id="d4a11-123">System.String</span></span>

## <span data-ttu-id="d4a11-124">輸出</span><span class="sxs-lookup"><span data-stu-id="d4a11-124">OUTPUTS</span></span>

### <span data-ttu-id="d4a11-125">PSServiceDiagnosticSettings 中的 OutputClasses。</span><span class="sxs-lookup"><span data-stu-id="d4a11-125">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

## <span data-ttu-id="d4a11-126">筆記</span><span class="sxs-lookup"><span data-stu-id="d4a11-126">NOTES</span></span>

## <span data-ttu-id="d4a11-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="d4a11-127">RELATED LINKS</span></span>

<span data-ttu-id="d4a11-128">[Set-AzDiagnosticSetting](./Set-AzDiagnosticSetting.md) 
[移除-AzDiagnosticSetting](./Remove-AzDiagnosticSetting.md)</span><span class="sxs-lookup"><span data-stu-id="d4a11-128">[Set-AzDiagnosticSetting](./Set-AzDiagnosticSetting.md)
[Remove-AzDiagnosticSetting](./Remove-AzDiagnosticSetting.md)</span></span>
