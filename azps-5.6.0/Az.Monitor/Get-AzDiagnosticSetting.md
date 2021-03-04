---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 60B497F6-98A2-4C60-B142-FF5CD123362D
online version: https://docs.microsoft.com/powershell/module/az.monitor/get-azdiagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDiagnosticSetting.md
ms.openlocfilehash: 9cfe797482485abccdce8e7094b3f5caadf554ad
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908938"
---
# <span data-ttu-id="079e7-101">Get-AzDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="079e7-101">Get-AzDiagnosticSetting</span></span>

## <span data-ttu-id="079e7-102">簡介</span><span class="sxs-lookup"><span data-stu-id="079e7-102">SYNOPSIS</span></span>
<span data-ttu-id="079e7-103">獲得記錄的類別和時間資料。</span><span class="sxs-lookup"><span data-stu-id="079e7-103">Gets the logged categories and time grains.</span></span>

## <span data-ttu-id="079e7-104">語法</span><span class="sxs-lookup"><span data-stu-id="079e7-104">SYNTAX</span></span>

```
Get-AzDiagnosticSetting [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="079e7-105">描述</span><span class="sxs-lookup"><span data-stu-id="079e7-105">DESCRIPTION</span></span>
<span data-ttu-id="079e7-106">**Get-AzDiagnosticSetting** Cmdlet 會取得為資源記錄的類別和時間紋理。</span><span class="sxs-lookup"><span data-stu-id="079e7-106">The **Get-AzDiagnosticSetting** cmdlet gets the categories and time grains that are logged for a resource.</span></span>
<span data-ttu-id="079e7-107">時間量是公制的匯總間隔。</span><span class="sxs-lookup"><span data-stu-id="079e7-107">A time grain is the aggregation interval of a metric.</span></span>

## <span data-ttu-id="079e7-108">例子</span><span class="sxs-lookup"><span data-stu-id="079e7-108">EXAMPLES</span></span>

### <span data-ttu-id="079e7-109">範例 1：取得記錄類別和時間資料的狀態</span><span class="sxs-lookup"><span data-stu-id="079e7-109">Example 1: Get the status of the logging categories and time grains</span></span>
```
PS C:\>Get-AzDiagnosticSetting -ResourceId "/subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.keyvault/KeyVaults/ContosoKeyVault"
StorageAccountId   : /subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.storage/accounts/ContosoStorageAccount
StorageAccountName : ContosoStorageAccount001
Metrics

Logs
Enabled  : True
Category : AuditEvent
```

<span data-ttu-id="079e7-110">此命令會獲得以 *ResourceId* of /subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.keyvault/KeyVaults/ContosoKeyVault/ContosoKeyVault 為 Azure 金鑰庫所記錄的類別和時間紋理。</span><span class="sxs-lookup"><span data-stu-id="079e7-110">This command gets the categories and time grains that are logged for an Azure Key Vault with a *ResourceId* of /subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.keyvault/KeyVaults/ContosoKeyVault.</span></span>

## <span data-ttu-id="079e7-111">參數</span><span class="sxs-lookup"><span data-stu-id="079e7-111">PARAMETERS</span></span>

### <span data-ttu-id="079e7-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="079e7-112">-DefaultProfile</span></span>
<span data-ttu-id="079e7-113">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="079e7-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="079e7-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="079e7-114">-Name</span></span>
<span data-ttu-id="079e7-115">診斷設定的名稱。</span><span class="sxs-lookup"><span data-stu-id="079e7-115">The name of the diagnostic setting.</span></span> <span data-ttu-id="079e7-116">如果未將通話預設為「服務」，請如前一個 API 一樣。</span><span class="sxs-lookup"><span data-stu-id="079e7-116">If not given the call default to "service" as it was in the previous API.</span></span>

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

### <span data-ttu-id="079e7-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="079e7-117">-ResourceId</span></span>
<span data-ttu-id="079e7-118">指定資源的識別碼。</span><span class="sxs-lookup"><span data-stu-id="079e7-118">Specifies the ID of the resource.</span></span>

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

### <span data-ttu-id="079e7-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="079e7-119">CommonParameters</span></span>
<span data-ttu-id="079e7-120">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="079e7-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="079e7-121">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="079e7-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="079e7-122">輸入</span><span class="sxs-lookup"><span data-stu-id="079e7-122">INPUTS</span></span>

### <span data-ttu-id="079e7-123">System.String</span><span class="sxs-lookup"><span data-stu-id="079e7-123">System.String</span></span>

## <span data-ttu-id="079e7-124">輸出</span><span class="sxs-lookup"><span data-stu-id="079e7-124">OUTPUTS</span></span>

### <span data-ttu-id="079e7-125">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="079e7-125">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

## <span data-ttu-id="079e7-126">筆記</span><span class="sxs-lookup"><span data-stu-id="079e7-126">NOTES</span></span>

## <span data-ttu-id="079e7-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="079e7-127">RELATED LINKS</span></span>

<span data-ttu-id="079e7-128">[Set-AzDiagnosticSetting](./Set-AzDiagnosticSetting.md) 
[Remove-AzDiagnosticSetting](./Remove-AzDiagnosticSetting.md)</span><span class="sxs-lookup"><span data-stu-id="079e7-128">[Set-AzDiagnosticSetting](./Set-AzDiagnosticSetting.md)
[Remove-AzDiagnosticSetting](./Remove-AzDiagnosticSetting.md)</span></span>
