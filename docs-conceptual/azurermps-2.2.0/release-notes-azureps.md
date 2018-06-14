---
title: Azure PowerShell 變更記錄 | Microsoft Docs
description: 這是在最新版中對 Azure powershell 所做的變更歷程記錄。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 05/18/2017
ms.openlocfilehash: ca25f3c66f8e8f4c64fc04275da2bd28e32d2f6c
ms.sourcegitcommit: c98e3a21037ebd82936828bcb544eed902b24212
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/08/2018
ms.locfileid: "34854608"
---
# <a name="release-notes"></a><span data-ttu-id="94de0-103">版本資訊</span><span class="sxs-lookup"><span data-stu-id="94de0-103">Release notes</span></span>

<span data-ttu-id="94de0-104">這是此版本中對 Azure PowerShell 所做的變更清單。</span><span class="sxs-lookup"><span data-stu-id="94de0-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

## <a name="version-220"></a><span data-ttu-id="94de0-105">2.2.0 版</span><span class="sxs-lookup"><span data-stu-id="94de0-105">Version 2.2.0</span></span>
* <span data-ttu-id="94de0-106">計算</span><span class="sxs-lookup"><span data-stu-id="94de0-106">Compute</span></span>
  - <span data-ttu-id="94de0-107">新增從 AzureDiskEncryptionForLinux 擴充查詢加密狀態的支援</span><span class="sxs-lookup"><span data-stu-id="94de0-107">Add support for querying encryption status from the AzureDiskEncryptionForLinux extension</span></span>
* <span data-ttu-id="94de0-108">DataFactory</span><span class="sxs-lookup"><span data-stu-id="94de0-108">DataFactory</span></span>
  - <span data-ttu-id="94de0-109">已新增 Cmdlet 以供列出活動時段</span><span class="sxs-lookup"><span data-stu-id="94de0-109">Added new cmdlet for listing activity windows</span></span>
    + <span data-ttu-id="94de0-110">Get-AzureRmDataFactoryActivityWindow</span><span class="sxs-lookup"><span data-stu-id="94de0-110">Get-AzureRmDataFactoryActivityWindow</span></span>
* <span data-ttu-id="94de0-111">DataLake</span><span class="sxs-lookup"><span data-stu-id="94de0-111">DataLake</span></span>
  - <span data-ttu-id="94de0-112">已將參數 `Host` 變更為 `DatabaseHost` 並將別名新增至 `Host`</span><span class="sxs-lookup"><span data-stu-id="94de0-112">Changed parameter `Host` to `DatabaseHost` and added alias to `Host`</span></span>
    + <span data-ttu-id="94de0-113">New-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="94de0-113">New-AzureRmDataLakeAnalyticsCatalogSecret</span></span>
    + <span data-ttu-id="94de0-114">Set-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="94de0-114">Set-AzureRmDataLakeAnalyticsCatalogSecret</span></span>
  - <span data-ttu-id="94de0-115">新增 ACL 和預設 ACL 移除的支援</span><span class="sxs-lookup"><span data-stu-id="94de0-115">Add support for ACL and Default ACL removal</span></span>
  - <span data-ttu-id="94de0-116">新增取得及設定檔案和資料夾之未命名權限的支援</span><span class="sxs-lookup"><span data-stu-id="94de0-116">Add support for getting and setting unnamed permissions on files and folders</span></span>
* <span data-ttu-id="94de0-117">KeyVault</span><span class="sxs-lookup"><span data-stu-id="94de0-117">KeyVault</span></span>
  - <span data-ttu-id="94de0-118">新增憑證的支援</span><span class="sxs-lookup"><span data-stu-id="94de0-118">Add support for certificates</span></span>
    + <span data-ttu-id="94de0-119">Add-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="94de0-119">Add-AzureKeyVaultCertificate</span></span>
    + <span data-ttu-id="94de0-120">Add-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="94de0-120">Add-AzureKeyVaultCertificateContact</span></span>
    + <span data-ttu-id="94de0-121">Get-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="94de0-121">Get-AzureKeyVaultCertificate</span></span>
    + <span data-ttu-id="94de0-122">Get-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="94de0-122">Get-AzureKeyVaultCertificateContact</span></span>
    + <span data-ttu-id="94de0-123">Get-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="94de0-123">Get-AzureKeyVaultCertificateIssuer</span></span>
    + <span data-ttu-id="94de0-124">Get-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="94de0-124">Get-AzureKeyVaultCertificateOperation</span></span>
    + <span data-ttu-id="94de0-125">Get-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="94de0-125">Get-AzureKeyVaultCertificatePolicy</span></span>
    + <span data-ttu-id="94de0-126">Import-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="94de0-126">Import-AzureKeyVaultCertificate</span></span>
    + <span data-ttu-id="94de0-127">New-AzureKeyVaultCertificateAdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="94de0-127">New-AzureKeyVaultCertificateAdministratorDetails</span></span>
    + <span data-ttu-id="94de0-128">New-AzureKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="94de0-128">New-AzureKeyVaultCertificateOrganizationDetails</span></span>
    + <span data-ttu-id="94de0-129">New-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="94de0-129">New-AzureKeyVaultCertificatePolicy</span></span>
    + <span data-ttu-id="94de0-130">Remove-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="94de0-130">Remove-AzureKeyVaultCertificate</span></span>
    + <span data-ttu-id="94de0-131">Remove-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="94de0-131">Remove-AzureKeyVaultCertificateContact</span></span>
    + <span data-ttu-id="94de0-132">Remove-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="94de0-132">Remove-AzureKeyVaultCertificateIssuer</span></span>
    + <span data-ttu-id="94de0-133">Remove-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="94de0-133">Remove-AzureKeyVaultCertificateOperation</span></span>
    + <span data-ttu-id="94de0-134">Set-AzureKeyVaultCertificateAttribute</span><span class="sxs-lookup"><span data-stu-id="94de0-134">Set-AzureKeyVaultCertificateAttribute</span></span>
    + <span data-ttu-id="94de0-135">Set-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="94de0-135">Set-AzureKeyVaultCertificateIssuer</span></span>
    + <span data-ttu-id="94de0-136">Set-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="94de0-136">Set-AzureKeyVaultCertificatePolicy</span></span>
    + <span data-ttu-id="94de0-137">Stop-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="94de0-137">Stop-AzureKeyVaultCertificateOperation</span></span>
* <span data-ttu-id="94de0-138">網路</span><span class="sxs-lookup"><span data-stu-id="94de0-138">Network</span></span>

  - <span data-ttu-id="94de0-139">新增網路介面的切換參數來啟用/停用加速網路 +New-AzureRmNetworkInterface -EnableAcceleratedNetworking</span><span class="sxs-lookup"><span data-stu-id="94de0-139">New switch parameter added for network interface to enable/disable accelerated networking +New-AzureRmNetworkInterface -EnableAcceleratedNetworking</span></span>
  - <span data-ttu-id="94de0-140">啟用主動-主動閘道功能 PowerShell Cmdlet</span><span class="sxs-lookup"><span data-stu-id="94de0-140">Enable Active-Active gateway feature PowerShell cmdlets</span></span>
    + <span data-ttu-id="94de0-141">Add-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="94de0-141">Add-AzureRmVirtualNetworkGatewayIpConfig</span></span>
    + <span data-ttu-id="94de0-142">Remove-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="94de0-142">Remove-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="94de0-143">已新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="94de0-143">Added new cmdlet</span></span>
    + <span data-ttu-id="94de0-144">Test-AzureRmPrivateIpAddressAvailability</span><span class="sxs-lookup"><span data-stu-id="94de0-144">Test-AzureRmPrivateIpAddressAvailability</span></span>
* <span data-ttu-id="94de0-145">資源</span><span class="sxs-lookup"><span data-stu-id="94de0-145">Resources</span></span>
  - <span data-ttu-id="94de0-146">支援提供者和資源 Cmdlet 的區域</span><span class="sxs-lookup"><span data-stu-id="94de0-146">Support zones in provider and resource cmdlets</span></span>
    + <span data-ttu-id="94de0-147">Get-AzureRmProvider</span><span class="sxs-lookup"><span data-stu-id="94de0-147">Get-AzureRmProvider</span></span>
    + <span data-ttu-id="94de0-148">New-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="94de0-148">New-AzureRmResource</span></span>
    + <span data-ttu-id="94de0-149">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="94de0-149">Set-AzureRmResource</span></span>
* <span data-ttu-id="94de0-150">Sql</span><span class="sxs-lookup"><span data-stu-id="94de0-150">Sql</span></span>
  - <span data-ttu-id="94de0-151">已在伺服器層級新增用於 Azure SQL 威脅偵測原則管理的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="94de0-151">Added new cmdlets for Azure SQL threat detection policy management at server level</span></span>
    + <span data-ttu-id="94de0-152">Get-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="94de0-152">Get-AzureRmSqlServerThreatDetectionPolicy</span></span>
    + <span data-ttu-id="94de0-153">Remove-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="94de0-153">Remove-AzureRmSqlServerThreatDetectionPolicy</span></span>
    + <span data-ttu-id="94de0-154">Set-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="94de0-154">Set-AzureRmSqlServerThreatDetectionPolicy</span></span>
  - <span data-ttu-id="94de0-155">已新增 Cmdlet 來支援為 Sql Azure DataWarehouse 啟用/停用 GeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="94de0-155">Added new cmdlets to support enabling/disabling GeoBackupPolicy for Sql Azure DataWarehouses</span></span>
    + <span data-ttu-id="94de0-156">Get-AzureRmSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="94de0-156">Get-AzureRmSqlDatabaseGeoBackupPolicy</span></span>
    + <span data-ttu-id="94de0-157">Set-AzureRmSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="94de0-157">Set-AzureRmSqlDatabaseGeoBackupPolicy</span></span>
  - <span data-ttu-id="94de0-158">已新增 Azure Sql Advisor 和建議動作 API 的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="94de0-158">Added new cmdlets for Azure Sql Advisors and Recommended Actions APIs</span></span>
    + <span data-ttu-id="94de0-159">Get-AzureRmSqlDatabaseAdvisor</span><span class="sxs-lookup"><span data-stu-id="94de0-159">Get-AzureRmSqlDatabaseAdvisor</span></span>
    + <span data-ttu-id="94de0-160">Get-AzureRmSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="94de0-160">Get-AzureRmSqlElasticPoolAdvisor</span></span>
    + <span data-ttu-id="94de0-161">Get-AzureRmSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="94de0-161">Get-AzureRmSqlServerAdvisor</span></span>
    + <span data-ttu-id="94de0-162">Get-AzureRmSqlDatabaseRecommendedActions</span><span class="sxs-lookup"><span data-stu-id="94de0-162">Get-AzureRmSqlDatabaseRecommendedActions</span></span>
    + <span data-ttu-id="94de0-163">Get-AzureRmSqlElasticPoolRecommendedActions</span><span class="sxs-lookup"><span data-stu-id="94de0-163">Get-AzureRmSqlElasticPoolRecommendedActions</span></span>
    + <span data-ttu-id="94de0-164">Get-AzureRmSqlServerRecommendedActions</span><span class="sxs-lookup"><span data-stu-id="94de0-164">Get-AzureRmSqlServerRecommendedActions</span></span>
    + <span data-ttu-id="94de0-165">Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="94de0-165">Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus</span></span>
    + <span data-ttu-id="94de0-166">Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="94de0-166">Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus</span></span>
    + <span data-ttu-id="94de0-167">Set-AzureRmSqlServerAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="94de0-167">Set-AzureRmSqlServerAdvisorAutoExecuteStatus</span></span>
    + <span data-ttu-id="94de0-168">Set-AzureRmSqlDatabaseRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="94de0-168">Set-AzureRmSqlDatabaseRecommendedActionState</span></span>
    + <span data-ttu-id="94de0-169">Set-AzureRmSqlElasticPoolRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="94de0-169">Set-AzureRmSqlElasticPoolRecommendedActionState</span></span>
    + <span data-ttu-id="94de0-170">Set-AzureRmSqlServerRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="94de0-170">Set-AzureRmSqlServerRecommendedActionState</span></span>
