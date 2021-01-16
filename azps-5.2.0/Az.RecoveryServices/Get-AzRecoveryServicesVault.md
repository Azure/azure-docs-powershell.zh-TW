---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 818B5302-91EE-425F-B1CD-86B626F1B7A3
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVault.md
ms.openlocfilehash: fcedf52f75b73cc35b7f0e4fd0856600bca6fc71
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98282568"
---
# <span data-ttu-id="e5dc5-101">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="e5dc5-101">Get-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="e5dc5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e5dc5-102">SYNOPSIS</span></span>

<span data-ttu-id="e5dc5-103">取得恢復服務電子倉庫的清單。</span><span class="sxs-lookup"><span data-stu-id="e5dc5-103">Gets a list of Recovery Services vaults.</span></span>

## <span data-ttu-id="e5dc5-104">句法</span><span class="sxs-lookup"><span data-stu-id="e5dc5-104">SYNTAX</span></span>

### <span data-ttu-id="e5dc5-105">ByTagNameValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5dc5-105">ByTagNameValueParameterSet</span></span>
```
Get-AzRecoveryServicesVault [[-ResourceGroupName] <String>] [[-Name] <String>] [-TagName <String>]
 [-TagValue <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5dc5-106">ByTagObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5dc5-106">ByTagObjectParameterSet</span></span>
```
Get-AzRecoveryServicesVault [[-ResourceGroupName] <String>] [[-Name] <String>] -Tag <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e5dc5-107">說明</span><span class="sxs-lookup"><span data-stu-id="e5dc5-107">DESCRIPTION</span></span>

<span data-ttu-id="e5dc5-108">**AzRecoveryServicesVault** Cmdlet 會在目前的訂閱中取得恢復服務電子倉庫的清單。</span><span class="sxs-lookup"><span data-stu-id="e5dc5-108">The **Get-AzRecoveryServicesVault** cmdlet gets a list of Recovery Services vaults in the current subscription.</span></span>

## <span data-ttu-id="e5dc5-109">示例</span><span class="sxs-lookup"><span data-stu-id="e5dc5-109">EXAMPLES</span></span>

### <span data-ttu-id="e5dc5-110">範例1</span><span class="sxs-lookup"><span data-stu-id="e5dc5-110">Example 1</span></span>

```powershell
PS C:\> Get-AzRecoveryServicesVault
```

<span data-ttu-id="e5dc5-111">在選取的訂閱中取得保存庫清單。</span><span class="sxs-lookup"><span data-stu-id="e5dc5-111">Get the list of vault in selected subscription.</span></span>

### <span data-ttu-id="e5dc5-112">範例2</span><span class="sxs-lookup"><span data-stu-id="e5dc5-112">Example 2</span></span>

```powershell
PS C:\> Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup"
```

<span data-ttu-id="e5dc5-113">在 [資源群組] 中取得選取訂閱的電子倉庫清單。</span><span class="sxs-lookup"><span data-stu-id="e5dc5-113">Get the list of vault in resource group in selected subscription.</span></span>

### <span data-ttu-id="e5dc5-114">範例3</span><span class="sxs-lookup"><span data-stu-id="e5dc5-114">Example 3</span></span>

```powershell
PS C:\> Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
```

<span data-ttu-id="e5dc5-115">在資源群組中取得具有指定名稱的電子倉庫。</span><span class="sxs-lookup"><span data-stu-id="e5dc5-115">Get the vault in resource group with given name.</span></span>

## <span data-ttu-id="e5dc5-116">參數</span><span class="sxs-lookup"><span data-stu-id="e5dc5-116">PARAMETERS</span></span>

### <span data-ttu-id="e5dc5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5dc5-117">-DefaultProfile</span></span>

<span data-ttu-id="e5dc5-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e5dc5-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e5dc5-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="e5dc5-119">-Name</span></span>

<span data-ttu-id="e5dc5-120">指定要查詢之保存庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="e5dc5-120">Specifies the name of the vault to query for.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5dc5-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5dc5-121">-ResourceGroupName</span></span>

<span data-ttu-id="e5dc5-122">指定要從哪個 Azure 資源群組中檢索指定的復原服務物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="e5dc5-122">Specifies the name of the Azure resource group from which to retrieve the specified Recovery Services object.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5dc5-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="e5dc5-123">-Tag</span></span>

<span data-ttu-id="e5dc5-124">指定要查詢的標記</span><span class="sxs-lookup"><span data-stu-id="e5dc5-124">Specifies the Tags to query for</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByTagObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5dc5-125">-TagName</span><span class="sxs-lookup"><span data-stu-id="e5dc5-125">-TagName</span></span>

<span data-ttu-id="e5dc5-126">指定要查詢的標記的索引鍵</span><span class="sxs-lookup"><span data-stu-id="e5dc5-126">Specifies the Key of the Tag to query for</span></span>

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5dc5-127">-TagValue</span><span class="sxs-lookup"><span data-stu-id="e5dc5-127">-TagValue</span></span>

<span data-ttu-id="e5dc5-128">指定要查詢的標記值</span><span class="sxs-lookup"><span data-stu-id="e5dc5-128">Specifies the Value of the Tag to query for</span></span>

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5dc5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5dc5-129">CommonParameters</span></span>
<span data-ttu-id="e5dc5-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e5dc5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5dc5-131">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e5dc5-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5dc5-132">輸入</span><span class="sxs-lookup"><span data-stu-id="e5dc5-132">INPUTS</span></span>

### <span data-ttu-id="e5dc5-133">所有</span><span class="sxs-lookup"><span data-stu-id="e5dc5-133">None</span></span>

## <span data-ttu-id="e5dc5-134">輸出</span><span class="sxs-lookup"><span data-stu-id="e5dc5-134">OUTPUTS</span></span>

### <span data-ttu-id="e5dc5-135">ARSVault 中的 RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e5dc5-135">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="e5dc5-136">筆記</span><span class="sxs-lookup"><span data-stu-id="e5dc5-136">NOTES</span></span>
<span data-ttu-id="e5dc5-137">Get-AzRecoveryServicesVault 舊版本的 Az. RecoveryServices ( # B0 = 2.10.0) 無法與 Az 搭配使用。 ( # B1 = 1.8.1) 的帳戶不正確的程式集參照。</span><span class="sxs-lookup"><span data-stu-id="e5dc5-137">Get-AzRecoveryServicesVault in old version of Az.RecoveryServices(<=2.10.0) cannot work with Az.Accounts(>=1.8.1) because of incorrect assembly reference.</span></span> <span data-ttu-id="e5dc5-138">如果您使用的是最新的 Az 或 Az，RecoveryServices 需要升級至2.11.0 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="e5dc5-138">The module Az.RecoveryServices needs to be upgraded to 2.11.0 or newer if you are using the latest Az or Az.Accounts.</span></span>

## <span data-ttu-id="e5dc5-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="e5dc5-139">RELATED LINKS</span></span>

[<span data-ttu-id="e5dc5-140">AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="e5dc5-140">Get-AzRecoveryServicesVaultSettingsFile</span></span>](./Get-AzRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="e5dc5-141">新-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="e5dc5-141">New-AzRecoveryServicesVault</span></span>](./New-AzRecoveryServicesVault.md)

[<span data-ttu-id="e5dc5-142">移除-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="e5dc5-142">Remove-AzRecoveryServicesVault</span></span>](./Remove-AzRecoveryServicesVault.md)
